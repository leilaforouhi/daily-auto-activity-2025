
import datetime
import hashlib

def generate_daily_hash():
    today = datetime.datetime.now().strftime("%Y-%m-%d %H:%M:%S")
    unique_hash = hashlib.sha256(today.encode()).hexdigest()
    return today, unique_hash

if __name__ == "__main__":
    timestamp, daily_hash = generate_daily_hash()
    print("Daily activity generated!")
    print(f"Timestamp: {timestamp}")
    print(f"Unique Hash: {daily_hash}")
