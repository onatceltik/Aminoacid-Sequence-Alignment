# Aminoacid-Sequence-Alignment
An aminoacid sequence alignment script that uses Needleman-Wunsch algorithm and BLOSUM62

It takes two aminoacid sequences (not case sensitive) and shows:
- partial scores table
- traceback table
- best alignment

Input:
```
Seq. #1: AGGCTATCACCTGACCTCCAGGCCGATGCCC
Seq. #2: TAGCTATCACGACCGCGGTCGATTTGCCCGAC
```
Output:
```
** PARTIAL SCORES TABLE **

      -    A    G    G    C    T    A    T    C    A    C    C    T    G    A    C    C    T    C    C    A    G    G    C    C    G    A    T    G    C    C    C
-     0  -10  -20  -30  -40  -50  -60  -70  -80  -90 -100 -110 -120 -130 -140 -150 -160 -170 -180 -190 -200 -210 -220 -230 -240 -250 -260 -270 -280 -290 -300 -310
T   -10    0  -10  -20  -30  -35  -45  -55  -65  -75  -85  -95 -105 -115 -125 -135 -145 -155 -165 -175 -185 -195 -205 -215 -225 -235 -245 -255 -265 -275 -285 -295
A   -20   -6    0  -10  -20  -30  -31  -41  -51  -61  -71  -81  -91 -101 -111 -121 -131 -141 -151 -161 -171 -181 -191 -201 -211 -221 -231 -241 -251 -261 -271 -281
G   -30  -16    0    6   -4  -14  -24  -33  -43  -51  -61  -71  -81  -85  -95 -105 -115 -125 -135 -145 -155 -165 -175 -185 -195 -205 -215 -225 -235 -245 -255 -265
C   -40  -26  -10   -3   15    5   -5  -15  -24  -34  -42  -52  -62  -72  -82  -86  -96 -106 -116 -126 -136 -146 -156 -166 -176 -186 -196 -206 -216 -226 -236 -246
T   -50  -36  -20  -12    5   20   10    0  -10  -20  -30  -40  -47  -57  -67  -77  -87  -91 -101 -111 -121 -131 -141 -151 -161 -171 -181 -191 -201 -211 -221 -231
A   -60  -46  -30  -20   -5   10   24   14    4   -6  -16  -26  -36  -46  -53  -63  -73  -83  -91 -101 -107 -117 -127 -137 -147 -157 -167 -177 -187 -197 -207 -217
T   -70  -56  -40  -30  -15    0   14   29   19    9   -1  -11  -21  -31  -41  -51  -61  -68  -78  -88  -98 -108 -118 -128 -138 -148 -157 -162 -172 -182 -192 -202
C   -80  -66  -50  -40  -21  -10    4   19   38   28   18    8   -2  -12  -22  -32  -42  -52  -59  -69  -79  -89  -99 -109 -119 -129 -139 -149 -159 -163 -173 -183
A   -90  -76  -60  -50  -31  -20   -6    9   28   42   32   22   12    2   -8  -18  -28  -38  -48  -58  -65  -75  -85  -95 -105 -115 -125 -135 -145 -155 -163 -173
C  -100  -86  -70  -60  -41  -30  -16   -1   18   32   51   41   31   21   11    1   -9  -19  -29  -39  -49  -59  -69  -76  -86  -96 -106 -116 -126 -136 -146 -154
G  -110  -96  -80  -64  -51  -40  -26  -11    8   22   41   48   39   37   27   17    7   -3  -13  -23  -33  -43  -53  -63  -73  -80  -90 -100 -110 -120 -130 -140
A  -120 -106  -90  -74  -61  -50  -36  -21   -2   12   31   41   48   39   41   31   21   11    1   -9  -19  -29  -39  -49  -59  -69  -76  -86  -96 -106 -116 -126
C  -130 -116 -100  -84  -65  -60  -46  -31  -12    2   21   40   40   45   39   50   40   30   20   10    0  -10  -20  -30  -40  -50  -60  -70  -80  -87  -97 -107
C  -140 -126 -110  -94  -75  -66  -56  -41  -22   -8   11   30   39   37   45   48   59   49   39   29   19    9   -1  -11  -21  -31  -41  -51  -61  -71  -78  -88
G  -150 -136 -120 -104  -85  -76  -66  -51  -32  -18    1   20   29   45   37   42   49   57   47   37   29   25   15    5   -5  -15  -25  -35  -45  -55  -65  -75
C  -160 -146 -130 -114  -95  -86  -76  -61  -42  -28   -9   10   19   35   45   46   51   48   66   56   46   36   26   24   14    4   -6  -16  -26  -36  -46  -56
G  -170 -156 -140 -124 -105  -96  -86  -71  -52  -38  -19    0    9   25   35   42   43   49   56   63   56   52   42   32   22   20   10    0  -10  -20  -30  -40
G  -180 -166 -150 -134 -115 -106  -96  -81  -62  -48  -29  -10   -1   15   25   32   39   41   46   53   63   62   58   48   38   28   20   10    6   -4  -14  -24
T  -190 -176 -160 -144 -125 -110 -106  -91  -72  -58  -39  -20   -5    5   15   24   31   44   40   45   53   61   60   57   47   37   28   25   15    5   -5  -15
C  -200 -186 -170 -154 -135 -120 -110 -101  -82  -68  -49  -30  -15   -5    5   24   33   34   53   49   45   51   58   69   66   56   46   36   26   24   14    4
G  -210 -196 -180 -164 -145 -130 -120 -111  -92  -78  -59  -40  -25   -9   -5   14   23   31   43   50   49   51   57   59   66   72   62   52   42   32   22   12
A  -220 -206 -190 -174 -155 -140 -126 -120 -102  -88  -69  -50  -35  -19   -5    4   14   23   33   43   54   49   51   57   59   66   76   66   56   46   36   26
T  -230 -216 -200 -184 -165 -150 -136 -121 -112  -98  -79  -60  -45  -29  -15   -6    4   19   23   33   44   52   47   50   56   57   66   81   71   61   51   41
T  -240 -226 -210 -194 -175 -160 -146 -131 -122 -108  -89  -70  -55  -39  -25  -16   -6    9   18   23   34   42   50   46   49   54   57   71   79   70   60   50
T  -250 -236 -220 -204 -185 -170 -156 -141 -132 -118  -99  -80  -65  -49  -35  -26  -16   -1    8   17   24   32   40   49   45   47   54   62   69   78   69   59
G  -260 -246 -230 -214 -195 -180 -166 -151 -142 -128 -109  -90  -75  -59  -45  -36  -26  -11   -2    7   17   30   38   39   46   51   47   52   68   68   75   66
C  -270 -256 -240 -224 -205 -190 -176 -161 -142 -138 -119 -100  -85  -69  -55  -36  -27  -21   -2    7    7   20   28   47   48   43   51   46   58   77   77   84
C  -280 -266 -250 -234 -215 -200 -186 -171 -152 -142 -129 -110  -95  -79  -65  -46  -27  -28  -12    7    7   10   18   37   56   46   43   50   48   67   86   86
C  -290 -276 -260 -244 -225 -210 -196 -181 -162 -152 -133 -120 -105  -89  -75  -56  -37  -28  -19   -3    7    4    8   27   46   53   46   42   47   57   76   95
G  -300 -286 -270 -254 -235 -220 -206 -191 -172 -162 -143 -130 -115  -99  -85  -66  -47  -38  -29  -13   -3   13   10   17   36   52   53   44   48   47   66   85
A  -310 -296 -280 -264 -245 -230 -216 -201 -182 -168 -153 -140 -125 -109  -95  -76  -57  -47  -38  -23   -9    3   13   10   26   42   56   53   44   48   56   75
C  -320 -306 -290 -274 -255 -240 -226 -211 -192 -178 -159 -144 -135 -119 -105  -86  -67  -57  -38  -29  -19   -7    3   22   19   32   46   55   50   53   57   65

** TRACEBACK TABLE **

      -    A    G    G    C    T    A    T    C    A    C    C    T    G    A    C    C    T    C    C    A    G    G    C    C    G    A    T    G    C    C    C
-  done left left left left left left left left left left left left left left left left left left left left left left left left left left left left left left left
T    up diag left left left diag left left left left left left left left left left left left left left left left left left left left left left left left left left
A    up diag diag left left left diag left left left left left left left left left left left left left left left left left left left left left left left left left
G    up   up diag diag left left left diag left diag left left left diag left left left left left left left left left left left left left left left left left left
C    up   up   up diag diag left left left diag left diag left left left left diag left left left left left left left left left left left left left left left left
T    up   up   up diag   up diag left left left left left left diag left left left left diag left left left left left left left left left left left left left left
A    up   up   up diag   up   up diag left left left left left left left diag left left left diag left diag left left left left left left left left left left left
T    up   up   up   up   up   up   up diag left left left left left left left left left diag left left left left left left left left diag diag left left left left
C    up   up   up   up diag   up   up   up diag left left left left left left left left left diag left left left left left left left left left left diag left left
A    up   up   up   up   up   up   up   up   up diag left left left left left left left left left left diag left left left left left left left left left diag left
C    up   up   up   up   up   up   up   up   up   up diag left left left left left left left left left left left left diag left left left left left left left diag
G    up   up   up diag   up   up   up   up   up   up   up diag diag diag left left left left left left left left left left left diag left left left left left left
A    up   up   up   up   up   up   up   up   up   up   up diag diag diag diag left left left left left left left left left left left diag left left left left left
C    up   up   up   up diag   up   up   up   up   up   up diag diag diag diag diag left left left left left left left left left left left left left diag left left
C    up   up   up   up   up diag   up   up   up   up   up   up diag diag diag diag diag left left left left left left left left left left left left left diag left
G    up   up   up   up   up   up   up   up   up   up   up   up   up diag diag diag   up diag left left diag diag left left left left left left left left left left
C    up   up   up   up   up   up   up   up   up   up   up   up   up   up diag diag diag diag diag left left left left diag left left left left left left left left
G    up   up   up   up   up   up   up   up   up   up   up   up   up   up   up diag diag diag   up diag diag diag left left left diag left left left left left left
G    up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up diag diag   up   up diag diag diag left left left diag left diag left left left
T    up   up   up   up   up diag   up   up   up   up   up   up diag   up   up diag diag diag diag diag   up diag diag diag left left diag diag left left left left
C    up   up   up   up   up   up diag   up   up   up   up   up   up   up   up diag diag   up diag diag diag   up diag diag diag left left left left diag left left
G    up   up   up   up   up   up   up   up   up   up   up   up   up diag   up   up   up diag   up diag diag diag diag   up diag diag left left left left left left
A    up   up   up   up   up   up diag diag   up   up   up   up   up   up diag   up diag diag   up diag diag diag diag diag diag diag diag left left left left left
T    up   up   up   up   up   up   up diag   up   up   up   up   up   up   up   up   up diag   up   up   up diag diag diag diag diag   up diag left left left left
T    up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up diag   up   up   up diag diag diag diag diag   up diag diag left left
T    up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up diag   up   up   up diag diag diag diag diag   up diag diag left
G    up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up diag diag diag   up diag diag diag   up diag   up diag diag
C    up   up   up   up   up   up   up   up diag   up   up   up   up   up   up diag diag   up diag diag   up   up   up diag diag diag diag diag   up diag diag diag
C    up   up   up   up   up   up   up   up   up diag   up   up   up   up   up   up diag diag   up diag diag   up   up   up diag left diag diag   up   up diag diag
C    up   up   up   up   up   up   up   up   up   up diag   up   up   up   up   up   up diag diag   up diag diag   up   up   up diag diag diag diag   up   up diag
G    up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up   up diag diag   up   up diag diag diag diag   up   up   up
A    up   up   up   up   up   up   up   up   up diag   up   up   up   up   up   up   up diag diag   up diag   up diag diag   up   up diag diag diag diag   up   up
C    up   up   up   up   up   up   up   up   up   up diag diag   up   up   up   up   up   up diag diag   up   up   up diag diag   up   up diag diag diag diag   up

** BEST ALIGNMENT **

Seq A: AGGCTATCACCTGACCTCCAGGC-CGATGCCC---
         ||||||||  |||| |  | |    |||||
Seq B: TAGCTATCAC--GACCGC-GGTCGATTTGCCCGAC

Best alignment score = 65
```
