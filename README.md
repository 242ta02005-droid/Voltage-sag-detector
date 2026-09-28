# Voltage-sag-detector
# Voltage Sag Detector

NORMAL_VOLTAGE = 230
SAG_LIMIT = 207   # 90% of 230 V

print("==============================")
print("      VOLTAGE SAG DETECTOR")
print("==============================")

voltage = float(input("Enter measured voltage (V): "))

print("\nMeasured Voltage:", voltage, "V")
print("Normal Voltage:", NORMAL_VOLTAGE, "V")

if voltage < SAG_LIMIT:
    sag_percentage = ((NORMAL_VOLTAGE - voltage) / NORMAL_VOLTAGE) * 100

    print("\n⚠️ VOLTAGE SAG DETECTED")
    print("Voltage reduction:", round(sag_percentage, 2), "%")
    print("🔴 Power quality is poor")

else:
    print("\n🟢 NO VOLTAGE SAG")
    print("✅ Voltage is within the normal range")
