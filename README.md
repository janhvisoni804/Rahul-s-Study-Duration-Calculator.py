n = int(input("Enter number of works: "))
for i in range(n):
    sh, sm, eh, em = map(int, input("Enter SH SM EH EM: ").split())
    start = sh * 60 + sm
    end = eh * 60 + em
    if end < start:
        end = end + 24 * 60
    time = end - start
    h = time // 60
    m = time % 60
    print("Duration:", h, "hour(s)", m, "minute(s)")
