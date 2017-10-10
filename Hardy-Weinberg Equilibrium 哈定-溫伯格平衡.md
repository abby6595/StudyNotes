# Section 2：Hardy-Weinberg Equilibrium 哈定-溫伯格平衡(?)

## 第三節：族群中的基因頻率與基因型頻率
### 哈溫平衡
* Hardy-Weinberg Equilibrium 是將 Mondel 遺傳放到一個廣大的人口群考量看人口中的對偶基因頻率Allele frequency ：
    1. 如何估計。
    2. 何時達到平衡（世代繁衍中保持不變）
    3. 會受到哪些因素影響，而無法保持平衡

* 可透過基因定型調查個體的基因型 genotype
    * 基因型 Genotype: 一生物個體內的DNA所包含的所有基因座(e.g. A, B,...etc) genetic locus 的allele組合。
        * Genotic locus A 會有 allele A,a 
* 基因型頻率可估對偶基因頻率Allele frequency)(aka 基因頻率 Gene frequency)
    * 基因頻率 Gene frequency: 特定 genetic locus 之 allele 在人群中的出現頻率。

For example, 對一個只有兩種allele A,a的genetical locus 進行 100人的定型：
|||AA|Aa|aa|Total|
---|---|---|---|---|---|
人數||30|60|10|100|
基因數|A|30*2=60|60*1=60|10*0=0|120
||a|30*0=0|60*1=60|10*2=20|80

* Gene frequency of A is f(A)=120/200=0.6
* .. f(a)=80/200=0.4

Mondel 存疑派的問題：
1. 這樣的頻率是否會隨世代繁衍而改變？
2. 短指基因為顯性基因，若以上述所說，則幾代之後應該會變成三人短指對一人正常？

### Hardy-Weinberg Equilibrium
假設只有兩種對偶基因A,a. f(A)=p, f(a)=q, p+q=1
Genotype與及frequency 如下：
||A|a
---|---|---|
A|AA(p^2^)|Aa(pq)
a|aA(pq)|aa(q^2^)

Genotype的分布如下：
AA|Aa|aa|
--|--|--|
p^2^|2pq|q^2^

而新一代的Gene frequency：
f(A)=p^2^+1/2(2pq)=p(p+q)=p(?)
f(a)=q^2^+1/2(2pq)=q(p+q)=q(?)

**Conclusion**
在下列情況下++基因頻率在世代繁衍中會保持不變++：
1. 交配隨機(無近親交配/族群不會太小，否則易出現極端值e.g.亞當夏娃近視)
2. 無明顯對抗因素(生育率存活率/移民/突變)

### Hardy-Weinberg Equilibrium 有什麼用途？
* 對於一個只有兩種allele (A,a)的 genetic locus而言，gene frequency 雖然以三種 genotype，但在總人數固定的條件下，其實只有兩個自由參數(p,q)，甚至只要有p,q任一一個參數(q=1-p)就能估出三種genotype的gene frequency
* 可估隱性疾病之致病gene frequency。很多先天性代謝疾病在兩個allele都是突變型(e.g. aa)才會發病。For example, 假設苯酮尿症(phenylketonuria, PKU)從55715中發現5病患，其疾病基因的頻率q=(5/55715)^0.5^=9.5*10^-3^，算罕見，但事實上異型合子(外表正常，但帶有疾病基因者)H~c~=2pq/(2pq+p^2^)=2q/1+p大約50人就有1人帶有疾病基因。

### 如何檢驗哈溫平衡
    基因定型後，如何判定基因型分佈是否偏離哈溫平衡的預測？
* 用卡方檢定。但若是樣本數小，違反使用卡方檢定(***x***^2^ test)之假設時，可採葉氏連續性校正，將分子扣除0.5後再平方；或是使用費雪精確檢定。
* ***x***^2^ = Σ^3^~i=1~ (O~i~ - E~i~)^2^/6129*2, ***df***=資料點參數-期望值參數
    * O~i~ - 基因型的觀察人數
    * E~i~ - 期望人數
        * 期望人數＝i之期望值*總觀察人數
    * df - 自由度
    
Example: 一項針對 6129 位受試者進行MN血型的分析，請問觀察值與預測值之間是否有顯著差異？

||MM|MN|NN|總共|
--|--|--|--|--|
觀察人數|1787|3037|1305|6129

1. df = 3 - 2 = 1
    * 資料點參數 - 兩個自由變動的類別 M,N + 總數n
    * 期望值參數 - 一個參數（因為只要一個allele frequncy p就可知其他三種）+ 總數n
2. f(M) = p = (1787*2+3037)/6129*2 = 0.539
3. f(N) = q = 1-0.539=0.461
4. Exp[f(MM)]=p^2^=0.291
5. Exp[f(MN)]=2pq=0.496
6. Exp[f(NN)]=q^2^=0.212
7. 乘上總觀察人數可得基因型之期望分佈

||M/M|M/N|N/N|
--|--|--|--|--|
期望人數|1782.7|3045.6|1300.7

8. ***x***^2^=0.0489
9. 查表發現該統計值對應p=0.9，小於1(0代表無偏差，卡方值愈大代表愈偏差)，得結論為沒有偏離哈溫平衡。

## 基因頻率的估算及其變異量
    考慮雙對偶基因 bi-allele所構成之genotype進行基因頻率估計時，若allele 數目增加時，如何進行allele frequency的點估計，以及若將變異量考慮進去的話變異量要如何計算。
* 兩種點估計法：伯恩斯坦法以及EM演算法
### 伯恩斯坦法
    對於沒有唯一對應的基因型，在求某一點時把所有不含該點的外表型當作一種genotype，透過扣除法來估算。
Example: 人類ABO血型有三種allele(I^B^, I^B^, i)，但在實際測量時只能測得四種外表形(?)（A[I^A^I^A^, I^A^i], B[I^B^I^B^, I^B^i], AB[I^A^I^B^], O[ii]）。現在對2060位成人進行血型判定，結果如下：
|A|B|AB|O
--|--|--|--|
862|365|131|702

令三種allele frequency分別為：f(I^A^)=p, f(I^B^)=q, f(i)=r
由於O型的人對應的genotype只有ii，因此r大約=f(O)^0.5^，但是p, q沒有唯一對應的genotype，因此用伯恩斯坦法來估計：
p大約=1-(q^2^+2qr+r^2^)^0.5^ = 1-(f(B+O))^0.5^
q大約=1-(p^2^+2pr+p^2^)^0.5^ = 1-(f(A+O))^0.5^

也就是在求I^A^頻率時，把所有不含I^A^的外表型想成是一種non-I^A^之allele所組成的genotype，因此f(non-I^A^)=(f(non-I^A^)^2^)^0.5^ => f(I^A^) = 1-f(non-I^A^)

最後可得p=0.2803, q=0.1287, r=0.5838

### EM 演算法
    透過期望式expectation與極大化maximization兩步驟疊代，幾回合之後估計值會小於某個預定門檻，也就是收斂converge(?)。
Example: 續上題
**Step1 - E step**
令C(A), C(B), C(O),C(AB)分別代表各血型的人數。在哈溫平衡條件下，各種genotype的Exp為：
(I^A^I^A^): x~1~ = C(A)*[p^2^/(p^2^+2pr)]
(I^A^i): x~2~ = C(A)*[2pr/(p^2^+2pr)]
(I^B^I^B^): x~3~ = C(B)*[q^2^/(q^2^+2qr)]
(I^B^i): x~4~ = C(B)*[2qr/(q^2^+2qr)]
(ii): x~5~ = C(O)
(I^A^I^B^): x~6~ = C(AB)
將從伯恩斯坦法算出的pqr代入上面的exp可得：
x~1~=166.8865, x~2~=695.1135, x~3~=36.2316
x~4~=328.7684, x~5~=702, x~6~=131

**Step2 - M step**
假設上面估出來的genotype數目為真正的數目，則allele frequency最大概似法估計值 maximum likelihood estimates可寫為：
p^\^^ = (2x~1~+x~2~+x~6~)/2(Σx~i~)
q^\^^ = (2x~3~+x~4~+x~6~)/2(Σx~i~)
r^\^^ = (2x~5~+x~2~+x~4~)/2(Σx~i~)

做完step1~2算是完成一回的recusive，接著可以用新的pqr再回去step1算新的x~1~\~x~6~，直至pqr估計值之和為1。

### 基因頻率的變異量
略

## 影響哈溫平衡的因素
### 適合度（天擇）
    有些疾病本身會導致適合度fitness降低，導致generation間的gene frequency不再維持不變。
Example: 以單一隱性基因所引起的白化症albinism為例，假設人口中盛行率為1/20000，並且fitness=0（完全不會產生下一代，不管是生物性或人為的理由），要過多久其盛行率才會降低成一半，也就是1/40000？
下圖為三種genotype的不同fitness：
||AA|Aa|aa|Total
--|--|--|--|--|
起始世代|p^2^|2pq|q^2^|1
Fitness|1|1|0
配子貢獻|p^2^|2pq|0|p^2^+2pq

假設第零代時，allele frequency標記為q~0~，我們可推算出每一代人口中allele frequency of a:
q~0~ = q
q~1~ = pq/(p2+2pq)=q/(p+2q)=q~0~/(1+q~0~)(?)
q~2~ = q1/(1+q~1~)=(q~0~/1+q~0~)/[1+(q~0~/1+q~0~)]
......
q~t~ = q~0~/(1+tq~0~)

如果要將gene frequency從q~0~降到q~t~，所需要的代數為：
t = (q~0~-q~t~)/q~0~q~t~ = (1/q~t~)-(1/q~0~)


### 近親繁殖 Inbreeding（非隨機交配）
    若有 inbreeding，由於雙親間具有血緣關係，違反隨機交配的條件導致哈溫不平衡。
Example: 植物自交self-fertilization在起始世代時：
p(AA)=1/4, p(Aa)=1/2, p(aa)=1/4，經過一代self-fertilication後：
p(AA)=(1/4)*1+(1/2)*1/4=3/8
p(Aa)=(1/2)*1/2=2/8
p(aa)=(1/4)*1+(1/2)*1/4=3/8

中間減少，兩旁增加，已偏離哈溫平衡。若再self-fertilization一次
p(AA)=(3/8)*1+(2/8)*1/4=7/16
p(Aa)=(2/8)*1/2=2/16
p(aa)=(3/8)*1+(2/8)*1/4=7/16

然侯檢查每一代的allele frequency

G1: p(A)=1/4+1/2*1/2=1/2
G2: p(A)=3/8+2/8*1/2=1/2
G3: p(A)=7/16+2/16*1/2=1/2

會發現allele frequency沒有變動。由此可推論，inbreeding對genotype的影響包含：
1. increase 同型合子homozygous(AA,aa)的frequency
2. decrease 異型合子heterozygous(Aa)的frequency
3. 對所有基因都有影響，而不像選形配種assortative mating，只會影響該「形」之基因。(?)

近親繁殖係數inbreeding coefficient用來量化inbreeding對gene frequency的效應。

Example: 人口中heterzygous的頻率為H，在哈溫平衡下的heterzygous的frequency為H~0~，coefficient F為：(?)
F = H~0~-H/H~0~，移項後可將H用F的函數來表示：
H = H~0~-H~0~F = H~0~(1-F) = 2pq(1-F)
也就是說，相對於隨機交配而言，heterzygous頻率所減少的幅度就是F。透過F和基偶基因頻率，便可算出三種genotype的頻率：
p(AA) = p^2^(1-F)+pF = p^2^+pqF
p(Aa) = 2pq(1-F) = 2pq-2pqF
p(aa) = q^2^(1-F)+qF = q^2^+pqF