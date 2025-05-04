##### Negacja
To zaprzeczenie wyrażenia o formie: **negacja z P**
$$
\begin{array}{c@{\quad}c}
\textbf{P} & \neg \textbf{P} \\ \hline
\text{F} & \text{T} \\
\text{T} & \text{F} \\
\end{array}
$$
##### Alternatywa (lub)
To wyrażenie o formie: **P lub Q**
$$
\begin{array}{c@{\quad}c}
\textbf{P} & \textbf{Q} & \mathbf{P} \vee  \mathbf{Q} \\ \hline
\text{F} & \text{F} & \text{F}\\
\text{F} & \text{T} & \text{T}\\
\text{T} & \text{F} & \text{T}\\
\text{T} & \text{T} & \text{T}\\
\end{array}
$$
##### Koniunkcja (i)
To wyrażenie o formie: **P i Q**
$$
\begin{array}{c@{\quad}c}
\textbf{P} & \textbf{Q} & \mathbf{P} \wedge  \mathbf{Q} \\ \hline
\text{F} & \text{F} & \text{F}\\
\text{F} & \text{T} & \text{F}\\
\text{T} & \text{F} & \text{F}\\
\text{T} & \text{T} & \text{T}\\
\end{array}
$$
##### Implikacja
To wyrażenie o formie: **Jeżeli P to Q**
$$
\begin{array}{c@{\quad}c}
\textbf{P} & \textbf{Q} & \mathbf{P} \Rightarrow  \mathbf{Q} \\ \hline
\text{F} & \text{F} & \text{T}\\
\text{F} & \text{T} & \text{T}\\
\text{T} & \text{F} & \text{F}\\
\text{T} & \text{T} & \text{T}\\
\end{array}
$$
$$
\begin{align}
P \Rightarrow Q &\Leftrightarrow \neg P \vee Q \\
P \Rightarrow Q &\Leftrightarrow \neg Q \Rightarrow \neg P
\end{align}
$$
##### Równoważność
To wyrażenie o formie: **P wtedy i tylko wtedy, gdy Q**
$$
\begin{array}{c@{\quad}c}
\textbf{P} & \textbf{Q} & \mathbf{P} \Leftrightarrow  \mathbf{Q} \\ \hline
\text{F} & \text{F} & \text{T}\\
\text{F} & \text{T} & \text{F}\\
\text{T} & \text{F} & \text{F}\\
\text{T} & \text{T} & \text{T}\\
\end{array}
$$
#Logika 