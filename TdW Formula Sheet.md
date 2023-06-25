# Thermodynamik
## 1. HS
$$
dU = \delta Q + dW
$$

## Ideales Gas
$$
dW = -pdV
$$
$$
pV = Nk_{B}T
$$
$$
P V=N R T, \quad d U=C_V N d T, \quad \delta W=-P d V
$$
$$
S_i\left(T_i, V_i\right)-S_i\left(T_i^{\mathrm{ref}}, V_i^{\mathrm{ref}}\right)=N_i C_V \log \left(T_i / T_i^{\mathrm{ref}}\right)+N_i R \log \left(V_i / V_i^{\mathrm{ref}}\right)
$$
## Absolute Temperatur
Die absolute Temperatur eines Reservoirs $R$ ist definiert als
$$
T:=\tau\left(R, R_{\mathrm{ref}}\right) T_{\mathrm{ref}} .
$$
Für das Verhältnis der mit einer nicht-trivialen reversiblen zyklischen Maschine ausgetauschten Wärmeflüsse mit zwei Reservoirs $R_1$ und $R_2$, definieren wir die Funktion
$$
\tau\left(R_1, R_2\right):=-\frac{Q_{R_1}}{Q_{R_2}} .
$$
## Skalierbare Systeme
Extensiv: Skaliert -> Homogen grad 1 (Volumen, Entropie, Teilchenzahl, Innere Energie)
Intensiv: gleich unabhängig von Größe -> Homogen grad 0
## Thermodynamische Potentiale
### Entropie
### Berrechnung von Entropie
Von Serie 6
![](Pasted%20image%2020230624142925.png)
![](Pasted%20image%2020230624142913.png)
#### Extremalprinzip der Entropie
Theorem 2.8 (**Extremalprinzip der Entropie**). Für $S \in \mathcal{S}$ und $\sigma \in \Sigma_S$ sowie jede mögliche disunkte Aufteilung von $S$ in Subsysteme $S^{\prime}, S^{\prime \prime} \in \mathcal{S}\left(S=S^{\prime} \vee S^{\prime \prime}\right)$ gilt
$$
S_S(\sigma)=\max _{\substack{\sigma^{\prime}, \sigma^{\prime \prime} \\\left(\sigma^{\prime}+\sigma^{\prime \prime}=\sigma\right)}} S_{S^{\prime}}\left(\sigma^{\prime}\right)+S_{S^{\prime \prime}}\left(\sigma^{\prime \prime}\right)
$$
wobei die Zustände $\sigma^{\prime} \in \Sigma_{S^{\prime}}$ und $\sigma^{\prime \prime} \in \Sigma_{S^{\prime \prime}}$ Zustände der Systeme $S^{\prime}$ und $S^{\prime \prime}$ sein sollen.
fun fact: Entropie ist additiv

#### Clausius Theorem
Für quaistatische Prozesse gilt
$$
\oint \frac{\delta Q_S}{T} \leq 0
$$
und falls $p$ rev ist sogar
$$
\oint \frac{\delta Q_S}{T}=0
$$

#### Entropiesatz
In einem adiabatischen Prozess kann die Entropie eines System nicht abnehmen, d.h. für einen adiabatischen Prozess $p \in \mathcal{P}$ auf einem System $S$ (der möglicherweise auch auf weitere Systeme wirkt), gilt
$$
S_S\left(\lfloor p\rfloor_S\right) \leq S_S\left(\lceil p\rceil_S\right)
$$
und es gilt Gleichheit, falls der Prozess rev ist.
**Beweis** 
führen $\sigma_2:=\lceil p\rceil_S$ über (alternativen) rev Prozess zurück nach $\sigma_1:=\lfloor p\rfloor_S$. Für ganzen Zyklus gilt
$$
0 \geq \oint \frac{\delta Q_S}{T}=\int_{\sigma_1}^{\sigma_2} \frac{\delta Q_S}{T}+\int_{\sigma_2}^{\sigma_1} \frac{\delta Q_S}{T}=\int_{\sigma_1}^{\sigma_2} \frac{\delta Q_S}{T}+S_S\left(\sigma_1\right)-S_S\left(\sigma_2\right)
$$
wobei bei der letzten Gleichung über einen reversiblen Weg zurück, somit Definition der Entropie direkt anwendbar. Weil Prozess von $\sigma_1$ nach $\sigma_2$ adiabatisch gilt $\delta Q_S=0$. Wir bekommen
$$
S_S\left(\sigma_2\right) \geq S_S\left(\sigma_1\right)
$$
Wenn $p$ selbst rev, müssen keinen alternativen Prozess finden, um $\sigma_2$ in $\sigma_1$ zurückzuführen. Weil $p$ adiabatischer rev Prozess ist folgt
$$
S_S\left(\sigma_2\right)-S_S\left(\sigma_1\right)=\int_{\sigma_1}^{\sigma_2} \frac{\delta Q_S}{T}=0 .
$$

## Innere Energie
$$
U=T S-p V+\mu N
$$
$$
U=F+T S
$$
#### Freie Helmholz Energie

$$
\begin{aligned}
F(T, V, N) & =-U^{*(S \rightarrow T)}(T, V, N) \\
& =\inf _S(U(S, V, N)-T S) \\
& =U(S, V, N)-T S \\
& =-p V+\mu N
\end{aligned}
$$
$$
\begin{aligned}
\mathrm{d} F & =\mathrm{d} U-T \mathrm{~d} S-S \mathrm{~d} T \\
& =T \mathrm{~d} S-p \mathrm{~d} V+\mu \mathrm{d} N-T \mathrm{~d} S-S \mathrm{~d} T \\
& =-p \mathrm{~d} V+\mu \mathrm{d} N-S \mathrm{~d} T
\end{aligned}
$$

### Entalpie
$$
\begin{aligned}
H(S, p, N) & =-U^{*(V \rightarrow-p)}(S, p, N) \\
& =\inf _V(U(S, V, N)+p V) \\
& =U(S, V, N)+p V \\
& =T S+\mu N,
\end{aligned}
$$


$$
\mathrm{d} H=\mathrm{d} U+p \mathrm{~d} V+V \mathrm{~d} p=T \mathrm{~d} S+V \mathrm{~d} p+\mu \mathrm{d} N
$$

### Gibbsche Freie energie
$$
\begin{aligned}
G(T, p, N) & =-U^{*(V \rightarrow-p, S \rightarrow T)}(T, p, N) \\
& =\inf _{S, V}(U(S, V, N)-T S+p V) \\
& =\inf _V(F(T, V, N)+p V) \\
& =\inf _S(H(S, p, N)-T S) \\
& =\mu(T, p) N .
\end{aligned}
$$
$$
\mathrm{d} G=\mathrm{d} U-\mathrm{d}(T S)+\mathrm{d}(p V)=-S \mathrm{~d} T+V \mathrm{~d} p+\mu \mathrm{d} N
$$
### Großkanonisches Potential
$$
\begin{aligned}
\Omega(T, V, \mu) & =-U^{*(S \rightarrow T, N \rightarrow \mu)}(T, V, \mu) \\
& =\inf _{S, N}(U(S, V, N)-T S-\mu N) \\
& =\inf _N(F(T, V, N)-\mu N) \\
& =-p(T, \mu) V \\
\end{aligned}
$$
$$
\mathrm{~d} \Omega =-S \mathrm{~d} T-p \mathrm{~d} V-N \mathrm{~d} \mu
$$
### Für konstantes N

$$
d F=-S d T-p d V, d H=T d S+V d p, \text { and } d G=-S d T+V d p
$$
$$
d U=T d S-p d V
$$
### Minimal und Maximalprinzip
Potential konkav & hom grad 1 $\implies$ Maximalprinzip (zB. für S)
Potential konvex & hom grad 1 $\implies$ Minimalprinzip  (zB. für F in V und T)
Die freie Energie $F(T, V, N)$ ist konkav in $T>0$ und konvex in $(V, N)$ (vgl. Theorem B.5 im Anhang). Analog zeigt man, dass die Enthalpie konkav in $p$ und konvex in $(S, N)$ ist. Außerdem ist die Gibbs'sche freie Energie konkav in $(T, p)$ und linear in $N .$ Das Großkanonische Potenzial $\Omega$ ist konkav in $(T, \mu)$ und linear in $V$.
$$
G^{\prime}\left(T, p, N_1^{\prime}, . ., N_r^{\prime}\right)+G^{\prime \prime}\left(T, p, N_1^{\prime \prime}, . ., N_r^{\prime \prime}\right) \geq G\left(T, p, N_1^{\prime}+N_1^{\prime \prime}, . ., N_r^{\prime}+N_r^{\prime \prime}\right)
$$
"Bei festen $T$ und $p$ ist die Gibbs'sche freie Energie im Gleichgewicht minimal."


## Maxwell relationen
$$
\left.\frac{\partial S}{\partial V}\right|_{T, N}=\left.\frac{\partial p}{\partial T}\right|_{V, N}, \quad-\left.\frac{\partial p}{\partial N}\right|_{T, V}=\left.\frac{\partial \mu}{\partial V}\right|_{T, N}, \quad-\left.\frac{\partial S}{\partial N}\right|_{T, V}=\left.\frac{\partial \mu}{\partial T}\right|_{V, N}
$$
$$
\begin{aligned}
& \left.\frac{\partial x}{\partial y}\right|_z=\left(\left.\frac{\partial y}{\partial x}\right|_z\right)^{-1}, \\
& -1=\left.\left.\left.\frac{\partial x}{\partial y}\right|_z \frac{\partial y}{\partial z}\right|_x \frac{\partial z}{\partial x}\right|_y, \\
& \left.\frac{\partial x}{\partial w}\right|_z=\left.\left.\frac{\partial x}{\partial y}\right|_z \frac{\partial y}{\partial w}\right|_z, \\
& \left.\frac{\partial x}{\partial z}\right|_w=\left.\left.\frac{\partial x}{\partial y}\right|_w \frac{\partial y}{\partial z}\right|_w, \\
& \left.\frac{\partial x}{\partial y}\right|_z=\left.\frac{\partial x}{\partial y}\right|_w+\left.\left.\frac{\partial x}{\partial w}\right|_y \frac{\partial w}{\partial y}\right|_z \cdot
\end{aligned}
$$
$$
\left. \frac{ \partial V }{ \partial p } \right|_{N} = - \left. \frac{ \partial N }{ \partial p } \right|_{V} \left. \frac{ \partial V }{ \partial N } \right|_{p} 
$$

## Clasius Clapeyron
$$
\left.\frac{\partial p}{\partial T} \equiv \frac{\partial p}{\partial T}\right|_{V, N}=\left.\frac{\partial S}{\partial V}\right|_{T, N}=\frac{S_2-S_1}{V_2-V_1}=\frac{L_{12}}{T\left(V_2-V_1\right)}
$$
mit $L_{12}$ der latenten wärme zwischen zustand 1 und 2 (verdampfungswärme, schmelzwärme)
## Gibbs Phasenregel
Für die einfachsten thermodynamischen Systeme lautet die Phasenregel:
$$
f=K-P+2
$$
$f$ : Anzahl der Freiheitsgrade des Systems
$K$ : Anzahl der unabhängigen Substanzen im System
$P:$ Anzahl der Phasen im System
## Gibbs Duhem Relation
$$
S \mathrm{~d} T-V \mathrm{~d} p+N \mathrm{~d} \mu=0 .
$$
Insbesondere sind nur zwei der drei Zustandsgrössen $T, p$ und $\mu$ unabhängig.

## Van der Waals Gas
- [ ] To Do

## Mischungen
- [ ] To Do

## Beispiele Thermodynamischer Systeme
### Diathermische Wand
![](Pasted%20image%2020230624135740.png)
### Bewegliche Adiabatische Wand
![](Pasted%20image%2020230624140430.png)
![](Pasted%20image%2020230624140442.png)

## Chemische Reaktionen
### Gleichgewichtskonstante
$$
\begin{aligned}
K(T, p) & =\exp \left(-\sum \nu_i g_i /(R T)\right) \\
& =\exp \left(-\left(2 g_1+1 g_2-2 g_3\right) /(R T)\right)
\end{aligned}
$$
# Statistische Mechanik
## Gleichverteilungssatz
$$
\left\langle  q_{i}\frac{ \partial H }{ \partial q_{j} }   \right\rangle =- \langle q_{i}\dot{p}_{j} \rangle  = k_{b}T \delta_{ij}
$$
## Ensembles/Gesamtheiten
![](PXL_20230530_101727249.jpg)
### Mikrokanonisches Ensemble
$V,N,E$ konstant
#### Zustand:
$$
\omega_{E}(x) = \frac{1}{\Sigma(E.N,V)}\delta(H(x)-E)
$$
#### Zustandssumme:
$$
\Sigma(E,N,V)\int_{\Gamma_{n}}^{} \delta(H(x)-E) \, dx 
$$
$\Gamma_{N}$ ist der konfigurationsraum
ausrechnen indem man die Zustandssumme über das gesamtvolumen bildet und dann ableitet 
$$
S(x) = \begin{cases}
0  & \text{for}  & x < 0 \\
1  &  & x \geq 0
\end{cases} \quad S^{\prime}(x) = \delta(x)
$$
#### Entropie
$$
S = k_{b}\log\left( \frac{\Sigma}{h^{3N}} \right)
$$
mit der Zustandssumme $\Sigma$
Herleitung:
$$
\tilde{S}(\tilde{\omega}):=-k_B \int_{\Gamma_N} \mathrm{~d} x \delta(H(x)-E) \tilde{\omega}(x) \log \tilde{\omega}(x) \equiv-k_B \int_{\{H(x)-E\}} \mathrm{d} x \tilde{\omega}(x) \log \tilde{\omega}(x)
$$

%%![](Pasted%20image%2020230524144219.png)%%
### Kanonisches Ensemble
fix: $V,N,T$
#### Zustand 
$$
\begin{aligned}
\omega(x) & =\omega_{V, N, T}(x) \\
& =\frac{e^{-\beta H(x)}}{Z(\beta)}
\end{aligned}
$$
$$
\beta=\frac{1}{k_B T}
$$

#### Zustandssumme
$$
Z(\beta)=\int_{\mathbb{R}^2} \frac{d p d q}{h^N} \mathrm{e}^{-\beta H(q, p)}
$$
with inverse temperature $\beta \equiv \frac{1}{k_B T}$ und anzahl dimensionen $N$.
oder im Diskreten fall:
$$
Z = \sum_{i}e^{-\beta E_{i}}
$$
where $E_{i}$ is the energy of microstate $i$. Propability that system is in microstate $i$:
$$
p_{i} = \frac{1}{Z}e^{ -\beta E_{i} }
$$
Intuition:
$$
Z=\int d E e^{-\beta E} \Sigma\left(E_1 V_1 N\right)
$$
#### Freie Energie
$$
F=-\beta^{-1} \log Z_1(\beta)=-k_{\mathrm{B}} T \log Z_1
$$
#### Entropie
$$
S=-\left(\frac{\partial F}{\partial T}\right)_V
$$
oder 
$$
S=-k_{\mathrm{B}} \int_{\mathbb{R}^2} \frac{d p d q}{h} \omega(q, p) \log \omega(q, p)  = -k_{b} \left< \log \omega \right> 
$$
#### Innere Energie
$$
U=F+T S
$$
$$
U = - \frac{ \partial  }{ \partial \beta } \log(Z(\beta))
$$
$$
U=\langle H\rangle=\int_{\mathbb{R}^2} \frac{d p d q}{h} \omega(q, p) H(q, p)
$$
#### Gaussian Integral
$$
\int_{-\infty}^{\infty} e^{ -a(x+b)^{2} } \, dx = \sqrt{ \frac{\pi}{a} }
$$
### Großkanonisches Ensemble
Fix: $V,T,\mu$
#### Zustand
$$
\omega(N, x)=\omega_{V_1, T_1}(N, x)
$$
$$
=\frac{e^{-\beta(H,(x)-\mu N)}}{\Xi(\beta, V, \mu)}
$$
#### Zustandssumme/Partition Sum:
$$
\Xi = \sum_{N = 0}^{\infty} \int_{\Gamma_{N}}^{} e^{ -\beta (H(x)-\mu N) } \, dx 
$$

Intuition:
$$
\Xi=\sum_{N=0}^{\infty} e^{\beta \mu N} Z(\beta, V, N)
$$
mit $Z$ Zustandssumme von kanonischer gesamtheit.

#### Großkanonisches Potential
$$
\Omega(\beta, V, N)=-\beta^{-1} \log \Xi (\beta, V, \mu)
$$
#### Averages
$$
\left\langle N_1\right\rangle=-\frac{\partial \Omega}{\partial \mu_1}
$$
$$
\langle N\rangle=\frac{1}{\Xi(\beta, \mu)} \sum_{N=0}^{\infty} \int_{\Gamma_N} d x N e^{-\beta(H(x)-\mu N)}=\frac{1}{\Xi(\beta, \mu)} \frac{1}{\beta} \frac{\partial}{\partial \mu} \Xi(\beta, \mu)
$$
$$
\langle p\rangle=-\frac{\partial \Omega}{\partial V}
$$
$$
S=-k\langle\log P\rangle=-\frac{\partial \Omega}{\partial T}
$$
$$
\langle E\rangle=\Omega+\left\langle N_1\right\rangle \mu_1 \ldots+\left\langle N_s\right\rangle \mu_s+S T
$$
## Verteilungen von bestimmten Systemen
### Kästchen / Energienieveaus
$K$ kästchen mit $N=\sum_{i=1}^K n_i$ teilchen gibt $N ! / \prod_i n_{i} !$ möglichkeiten. Entropie ist deshalb
$$
S=k_B \log N !-k_B \sum_i \log \left(n_{i} !\right)
$$
# Mathematik
## Satz von Gauss
$$
-p \oint_S \vec{r} \cdot d \vec{S}=-p \int_V \vec{\nabla} \cdot \vec{r} d V
$$

## Gaussian Integral
$$
\int_{-\infty}^{\infty} e^{ -a(x+b)^{2} } \, dx = \sqrt{ \frac{\pi}{a} }
$$
## Stirling Approximation
$$
\log N !=N \log N-N \quad \text{for} \quad N\gg 1
$$


## Lagrange Multiplier
minimize $f$ subject to constraint $g(x) =0$. For example $\sum n_{i} =N$:
$$
\mathcal{L}(x, \lambda) \equiv f(x)+\lambda \cdot g(x)
$$
$$
\frac{\partial \mathcal{L}}{\partial x}=0 \quad \text { and } \quad \frac{\partial \mathcal{L}}{\partial \lambda}=0 ;
$$
## Legrendre Transformation
$$
f^*(p):=\mathcal{L} f(p)=\sup _x[x p-f(x)]
$$
falls $f$ diff-bar $\implies$ $$
f^*(p)=\tilde{x} p-f(\tilde{x})
$$
where $\tilde{x}$  is defined by $p=f^{\prime}(\tilde{x})$.
The LT fulfills that 
$$
f^{* \prime}(p)=f^{\prime-1}(p)
$$
and $$
f^{* *}(x)=f(x)
$$
wenn $f$ differenzierbar und strikt konvex.
![](Pasted%20image%2020230625224748.png)

## Konvex Function
$$
f\left(\lambda x_1+(1-\lambda) x_2\right) \leq \lambda f\left(x_1\right)+(1-\lambda) f\left(x_2\right) \quad \forall \lambda \in[0,1]
$$