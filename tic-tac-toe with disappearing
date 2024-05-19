test = True

sec = [[-1, 0, 1], [-2, 0, 2], [-3, 0, 3], [-4, 0, 4], [-5, 0, 5], [-6, 0, 6], [-7, 0, 7], [-8, 0, 8], [-9, 0, 9]]
secO = sec
key = 0
choice = [0, 0, 0, 0, 0, 0, 0, 0, 0]
priority_move = []
priority_summ = []
w_key = 0
n = int(input('1 - ❌\t   '
              '2 - ⭕️\n'
              'Кто ходит первый?: '))


def value(x):
    if x == -1:
        return "1️⃣"
    if x == -2:
        return "2️⃣"
    if x == -3:
        return "3️⃣"
    if x == -4:
        return "4️⃣"
    if x == -5:
        return "5️⃣"
    if x == -6:
        return "6️⃣"
    if x == -7:
        return "7️⃣"
    if x == -8:
        return "8️⃣"
    if x == -9:
        return "9️⃣"
    if x == 2:
        return "⭕️"
    if x == 3:
        return "❌"


def result():
    if ((sec[0][0] == sec[1][0] == sec[2][0] == 2) or
            (sec[3][0] == sec[4][0] == sec[5][0] == 2) or
            (sec[6][0] == sec[7][0] == sec[8][0] == 2) or
            (sec[0][0] == sec[3][0] == sec[6][0] == 2) or
            (sec[1][0] == sec[4][0] == sec[7][0] == 2) or
            (sec[2][0] == sec[5][0] == sec[8][0] == 2) or
            (sec[0][0] == sec[4][0] == sec[8][0] == 2) or
            (sec[2][0] == sec[4][0] == sec[6][0] == 2)):
        return "Вы проиграли!"
    elif ((sec[0][0] == sec[1][0] == sec[2][0] == 3) or
          (sec[3][0] == sec[4][0] == sec[5][0] == 3) or
          (sec[6][0] == sec[7][0] == sec[8][0] == 3) or
          (sec[0][0] == sec[3][0] == sec[6][0] == 3) or
          (sec[1][0] == sec[4][0] == sec[7][0] == 3) or
          (sec[2][0] == sec[5][0] == sec[8][0] == 3) or
          (sec[0][0] == sec[4][0] == sec[8][0] == 3) or
          (sec[2][0] == sec[4][0] == sec[6][0] == 3)):
        return "Вы победили!"
    else:
        return "Ничья!"


def transl(arr1_sec, x, arr2_choice):
    if arr1_sec[x][1] == 5:
        arr1_sec[x][0] = arr1_sec[x][2] * -1
        arr1_sec[x][1] = 0
        arr2_choice[x] = 0
        return value(arr1_sec[x][0])
    else:
        return value(arr1_sec[x][0])


def typ(arr_sec, x):
    if (arr_sec[x][0] < 0) or (arr_sec[x][0] == 2):
        return 1


def near(x):
    summ = 0
    if x == 0:
        summ += ((typ(sec, 0) == typ(sec, 1) == typ(sec, 2)) + (typ(sec, 0) == typ(sec, 3) == typ(sec, 6)) +
                 (typ(sec, 0) == typ(sec, 4) == typ(sec, 8)))
    if x == 1:
        summ += (typ(sec, 0) == typ(sec, 1) == typ(sec, 2)) + (typ(sec, 1) == typ(sec, 4) == typ(sec, 7))

    if x == 2:
        summ += ((typ(sec, 0) == typ(sec, 1) == typ(sec, 2)) + (typ(sec, 2) == typ(sec, 5) == typ(sec, 8)) +
                 (typ(sec, 2) == typ(sec, 4) == typ(sec, 6)))
    if x == 3:
        summ += (typ(sec, 0) == typ(sec, 3) == typ(sec, 6)) + (typ(sec, 3) == typ(sec, 4) == typ(sec, 5))

    if x == 4:
        summ += ((typ(sec, 1) == typ(sec, 4) == typ(sec, 7)) + (typ(sec, 3) == typ(sec, 4) == typ(sec, 5)) +
                 (typ(sec, 0) == typ(sec, 4) == typ(sec, 8) + typ(sec, 2) == typ(sec, 4) == typ(sec, 6)))

    if x == 5:
        summ += (typ(sec, 2) == typ(sec, 5) == typ(sec, 8)) + (typ(sec, 3) == typ(sec, 4) == typ(sec, 5))

    if x == 6:
        summ += ((typ(sec, 2) == typ(sec, 4) == typ(sec, 6)) + (typ(sec, 0) == typ(sec, 3) == typ(sec, 6)) +
                 (typ(sec, 6) == typ(sec, 7) == typ(sec, 8)))

    if x == 7:
        summ += (typ(sec, 6) == typ(sec, 7) == typ(sec, 8)) + (typ(sec, 1) == typ(sec, 4) == typ(sec, 7))

    if x == 8:
        summ += ((typ(sec, 0) == typ(sec, 4) == typ(sec, 8)) + (typ(sec, 2) == typ(sec, 5) == typ(sec, 8)) +
                 (typ(sec, 6) == typ(sec, 7) == typ(sec, 8)))
    if summ > 0:
        return 1
    else:
        return 0


def nous(arr_sec, x):
    nous_xod = arr_sec[x][0]
    arr_sec[x][0] = 3
    if (True == (arr_sec[0][0] == arr_sec[1][0] == arr_sec[2][0]) or
            True == (arr_sec[3][0] == arr_sec[4][0] == arr_sec[5][0]) or
            True == (arr_sec[6][0] == arr_sec[7][0] == arr_sec[8][0]) or
            True == (arr_sec[0][0] == arr_sec[3][0] == arr_sec[6][0]) or
            True == (arr_sec[1][0] == arr_sec[4][0] == arr_sec[7][0]) or
            True == (arr_sec[2][0] == arr_sec[5][0] == arr_sec[8][0]) or
            True == (arr_sec[0][0] == arr_sec[4][0] == arr_sec[8][0]) or
            True == (arr_sec[2][0] == arr_sec[4][0] == arr_sec[6][0])):
        arr_sec[x][0] = nous_xod
        priority_move.append(x)
        priority_summ.append(5)
        return 2
    arr_sec[x][0] = 2
    if (True == (arr_sec[0][0] == arr_sec[1][0] == arr_sec[2][0]) or
            True == (arr_sec[3][0] == arr_sec[4][0] == arr_sec[5][0]) or
            True == (arr_sec[6][0] == arr_sec[7][0] == arr_sec[8][0]) or
            True == (arr_sec[0][0] == arr_sec[3][0] == arr_sec[6][0]) or
            True == (arr_sec[1][0] == arr_sec[4][0] == arr_sec[7][0]) or
            True == (arr_sec[2][0] == arr_sec[5][0] == arr_sec[8][0]) or
            True == (arr_sec[0][0] == arr_sec[4][0] == arr_sec[8][0]) or
            True == (arr_sec[2][0] == arr_sec[4][0] == arr_sec[6][0])):
        secO[x][0] = nous_xod
        priority_move.append(x)
        priority_summ.append(6)
        return 2
    arr_sec[x][0] = nous_xod
    if x == 4 and arr_sec[4][0] < 0:
        priority_move.append(x)
        priority_summ.append(4)
        return 2
    if x % 2 == 0 and arr_sec[x][0] < 0:
        priority_move.append(x)
        priority_summ.append(2+near(x))
        return 2
    if x % 2 == 0 and arr_sec[x][0] < 0:
        priority_move.append(x)
        priority_summ.append(2+near(x))
        return 2
    if x % 2 != 0 and arr_sec[x][0] < 0:
        priority_move.append(x)
        priority_summ.append(1)
        return 2


def que(arr1_sec, x):
    if arr1_sec[x][1] != 0:
        arr1_sec[x][1] += 1


if n == 2:
    i = -1
    key = 0
    w_key = 0

    while key == 0 and i < 8:
        i += 1
        if choice[i] == 0:
            secO = sec
            nous(secO, i)
    if test:
        print(priority_move)
        print(priority_summ)
    if 0 in choice:
        max_value = max(priority_summ)
        max_index = priority_summ.index(max_value)
        sec[priority_move[max_index]][0] = 2
        sec[priority_move[max_index]][1] = 1
        choice[priority_move[max_index]] = 1
        priority_move.clear()
        priority_summ.clear()
        print("||||||||||||||||||||||||||\n||\t\t||\t\t||\t\t||\n||\t",
              transl(sec, 0, choice), "||\t", transl(sec, 1, choice),
              "||\t", transl(sec, 2, choice),
              "||\n||\t" "\t||\t" "\t||\t" "\t||\n||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
              transl(sec, 3, choice), "||\t", transl(sec, 4, choice), "||\t", transl(sec, 5, choice),
              "||\n||\t" "\t||\t" "\t||\t" "\t||\n||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
              transl(sec, 6, choice), "||\t", transl(sec, 7, choice), "||\t", transl(sec, 8, choice),
              "||\n||\t" "\t||\t" "\t||\t" "\t||\n||||||||||||||||||||||||||")
    else:
        key = 1
else:
    print("||||||||||||||||||||||||||\n||\t\t||\t\t||\t\t||\n||\t",
          transl(sec, 0, choice), "||\t", transl(sec, 1, choice),
          "||\t", transl(sec, 2, choice),
          "||\n||\t" "\t||\t" "\t||\t" "\t||\n||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
          transl(sec, 3, choice), "||\t", transl(sec, 4, choice), "||\t", transl(sec, 5, choice),
          "||\n||\t" "\t||\t" "\t||\t" "\t||\n||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
          transl(sec, 6, choice), "||\t", transl(sec, 7, choice), "||\t", transl(sec, 8, choice),
          "||\n||\t" "\t||\t" "\t||\t" "\t||\n||||||||||||||||||||||||||")

while (((sec[0][0] != sec[1][0]) or (sec[1][0] != sec[2][0])) and (
        (sec[3][0] != sec[4][0]) or (sec[4][0] != sec[5][0])) and
       ((sec[6][0] != sec[7][0]) or (sec[7][0] != sec[8][0])) and
       ((sec[0][0] != sec[3][0]) or (sec[3][0] != sec[6][0])) and (
               (sec[1][0] != sec[4][0]) or (sec[4][0] != sec[7][0])) and
       ((sec[2][0] != sec[5][0]) or (sec[5][0] != sec[8][0])) and
       ((sec[0][0] != sec[4][0]) or (sec[4][0] != sec[8][0])) and (
               (sec[2][0] != sec[4][0]) or (sec[4][0] != sec[6][0]))) and key == 0:
    while w_key == 0:
        move = int(input('Введите номер ячейки для хода: ')) - 1
        if move in [0, 1, 2, 3, 4, 5, 6, 7, 8]:
            if choice[move] == 0:
                sec[move][0] = 3
                sec[move][1] = 1
                choice[move] = 1
                w_key = 1
    i = -1
    key = 0
    w_key = 0
    while key == 0 and i < 8:
        i += 1
        if choice[i] == 0:
            secO = sec
            nous(secO, i)
    if test:
        print(priority_move)
        print(priority_summ)
    if 0 in choice:
        max_value = max(priority_summ)
        max_index = priority_summ.index(max_value)
        sec[priority_move[max_index]][0] = 2
        sec[priority_move[max_index]][1] = 1
        choice[priority_move[max_index]] = 1
        priority_move.clear()
        priority_summ.clear()
    else:
        key = 1
    for i in range(9):
        que(sec, i)
    print("||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
          transl(sec, 0, choice), "||\t", transl(sec, 1, choice), "||\t", transl(sec, 2, choice), "||\n||\t"
          "\t||\t" "\t||\t" "\t||\n"
          "||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
          transl(sec, 3, choice), "||\t", transl(sec, 4, choice), "||\t", transl(sec, 5, choice), "||\n||\t"
          "\t||\t" "\t||\t" "\t||\n"
          "||||||||||||||||||||||||||\n||\t" "\t||\t" "\t||\t" "\t||\n||\t",
          transl(sec, 6, choice), "||\t", transl(sec, 7, choice), "||\t", transl(sec, 8, choice), "||\n||\t"
          "\t||\t" "\t||\t" "\t||\n"
          "||||||||||||||||||||||||||")
print(result())
