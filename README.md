def main():
    data = [
        ("P1", "VSCode", 100, "MID"),
        ("P23", "Eclipse", 234, "MID"),
        ("P93", "Chrome", 189, "High"),
        ("P42", "JDK", 9, "High"),
        ("P9", "CMD", 7, "High"),
        ("P87", "NotePad", 23, "Low")
    ]

    print("Assignment: Flight Table")
    print("P_ID\tProcess\tStart Time (ms)\tPriority")
    for row in data:
        print(f"{row[0]}\t{row[1]}\t{row[2]}\t\t{row[3]}")

    print("\nSort Options:")
    print("1. Sort by P_ID")
    print("2. Sort by Start Time")
    print("3. Sort by Priority")

    choice = int(input("Enter your choice: "))
    
    if choice == 1:
        data.sort(key=lambda x: x[0])
    elif choice == 2:
        data.sort(key=lambda x: x[2])
    elif choice == 3:
        data.sort(key=lambda x: x[3])
    else:
        print("Invalid choice. Sorting by P_ID (default)")
        data.sort(key=lambda x: x[0])

    print("\nSorted Result:")
    print("P_ID\tProcess\tStart Time (ms)\tPriority")
    for row in data:
        print(f"{row[0]}\t{row[1]}\t{row[2]}\t\t{row[3]}")

if __name__ == "__main__":
    main()
