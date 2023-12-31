---
layout: default
title: Эмпирическая функция распределения
nav_order: 1
---

# Эмпирическая функция распределения.
## Определение.


## Напоминание
\begin{definition}
   Оценка (точечная) -- любая функция от элементов выборки 
   $$\hat{\theta}_n(\xi_1,..., \xi_n)$$ 
   со значениями в \textbf{параметрическом множестве} $\Theta$, 
которая каким-то образом аппроксимирует неизвестный параметр.

\end{definition}

\begin{definition}
Оценки (любые) в статистике называются \textbf{статистиками}.
Т.е. СТАТИСТИКА - любая оценка (как объект в МС).

\end{definition}



\end{frame}


\begin{frame}{Выборка}
В МС у нас есть результаты эксперимента. И нужно сделать вывод о свойствах самого эксперимента.  
$$
x_1,x_2, ...., x_n.
$$

Мы хотим по элементам выборки воссоздать (аппроксимировать) ф.р..

\end{frame}

\begin{frame}{Эмпирическая функция распределения. Определение.}


\begin{definition}
     \textbf{Эмпирическая функция распределения}:
     \begin{eqnarray}
         \hat{F_n}(x;~x_1,...,x_n) 
         \overset{\mathrm{def}}{=}
         \frac{1}{n}\sum_{i=1}^n
         %\mathbbm{1}
         \mathds{1}_{\{\xi_i \leqslant x \}}
     \end{eqnarray}
\end{definition}

 
эмпирическая ф.р.  (оценка)  зависит от вещественного числа $x$ и от элементов выборки

\end{frame}

\begin{frame}{Упорядоченная выборка:}
\begin{definition}
    Упорядоченная выборка:
    $$
    x_{(1)}~\leqslant~x_{(2)}~\leqslant~ ....~\leqslant~ x_{(n)}
    $$
    называется \textbf{вариационным рядом},
    \\
    а элементы этого ряда 
    $$x_{(k)}$$
    называются  \textbf{ $k$-ми порядковыми статистиками} (или статистиками порядка $k$).
\end{definition}

\end{frame}


\begin{frame}{График Э.Ф.Р.}

    
\end{frame}{}


\subsection{Несмещённость и состоятельность оценки $\hat{F_n}$}


\begin{frame}{Несмещённость и состоятельность оценки $\hat{F_n}$}
\begin{enumerate}
    \item 
    \textbf{Утверждение 1.~~}
 $$\forall x \in  \mathbb{R} ~~~\hat{F_n}(x;~ \xi_1,\xi_2,...,\xi_n)$$ --
есть
несмещенная оценка числа $F_{\xi_i}(x)$.
\end{enumerate}
Док-во:
\begin{align*}
\mathrm{\mathbf{E}} \hat{F_n}(x;~ \xi_1,\xi_2,...,\xi_n) & =
\\
\mathrm{\mathbf{E}} \bigg( \frac{1}{n}\sum_{i=1}^n
         %\mathbbm{1}
         \mathds{1}_{\{\xi_i \leqslant x \}} \mathrm{\mathbf{E}} \bigg) & =
\frac{1}{n} \mathrm{\mathbf{E}} \sum_{i=1}^n
         %\mathbbm{1}
         \mathds{1}_{\{\xi_i \leqslant x \}}  =
         \\
\frac{1}{n}  \sum_{i=1}^n
         %\mathbbm{1}
         \mathrm{\mathbf{E}} \mathds{1}_{\{\xi_i \leqslant x \}} & =
        \frac{1}{n}  \sum_{i=1}^n
         %\mathbbm{1}
         \mathrm{P} \{\xi_i \leqslant x \}  
         \overset{\mathrm{def}}{=}
         F_{\xi_i}(x).
\end{align*}


\end{frame}{}

\begin{frame}{Несмещённость и состоятельность оценки $\hat{F_n}$}
\begin{enumerate}[2]
    \item 
    \textbf{Утверждение 2.~~}
$$\forall x \in  \mathbb{R} ~~~\hat{F_n}(x;~ \xi_1,\xi_2,...,\xi_n)$$ --
есть
состоятельная оценка числа $F_{\xi_i}(x)$.
\end{enumerate}
Док-во (следствие (У)ЗБЧ):
$$
\mathrm{P} ( \mathds {1}_{ \{\xi_i \leqslant x\} }=1 ) =
\mathrm{P} ( \xi_i \leqslant x ) = F_{\xi_i} (x),
$$
\begin{align*}
\frac{ 
\mathds{1}_{ \{\xi_1 \leqslant x\} }
 ~ + ~...~+~
 \mathds{1}_{ \{\xi_n \leqslant x\} }
}
{n}
\xrightarrow[n \to \infty]{\text{п.н.}}
~~F_{\xi_i}.
\end{align*}

\end{frame}{}


\subsection{Теорема Гливенко – Кантелли.}


\begin{frame}{Теорема Гливенко – Кантелли}
$F_{\xi_i}(x)$ равномерно хорошо приближается $\hat{F_n}(x; \xi_1,...,\xi_n)$ не просто в одной точке, а на все числовой оси.

\begin{theorem}
\textbf{Теорема Гливенко -- Кантелли.}
\begin{eqnarray*}
    \mathrm{P}\bigg( \sup_{x \in  \mathbb{R}} 
    \big| \hat{F_n}(x; \xi_1,...,\xi_n) ~-~ F_{\xi}(x) \big|
    \xrightarrow[n \to \infty]{ } 0
    \bigg) =1.
\end{eqnarray*}
\end{theorem}
То есть для почти любого исхода который,
существует  в  пространстве $\Omega$, где определены  случайные величины $\xi_1,...,\xi_n$, фактически для почти любой
выборки, которая может породиться в рамках нашего эксперимента, не только эта разность близко к нулю, но даже супремум по всей
числовой
прямой.
\end{frame}

\subsection{Теорема Колмогорова}

\begin{frame}{Теорема Колмогорова}
\begin{theorem}
\textbf{Теорема Колмогорова.}
Пусть
$F_{\xi_i}$- непрерывная и пусть
\begin{eqnarray*}
\sqrt{n}D_n=
\sqrt{n}
\sup_{x \in  \mathbb{R}} 
    \big| \hat{F_n}(x; \xi_1,...,\xi_n) ~-~ F_{\xi}(x) \big|,
\end{eqnarray*}
тогда
\begin{eqnarray*}
\sqrt{n}D_n
    \xrightarrow[n \to \infty]{D}
    \eta:~~~~
    \\F_{\eta}(y)=
     \begin{cases}
      0 & \text{если $y \leqslant 0$ }\\
      \sum_{i=-\infty}^{\infty} (-1)^i e^{-2i^2y^2} & \text{если $y > 0$ },
    \end{cases}
\end{eqnarray*}
где $F_{\eta}(y)$ -- распределение Колмогорова.
\end{theorem}
\end{frame}

\section{Функция риска}

\begin{frame}{}
Еще  один способ сравнивать оценки точечные оценки.
Дано (как и всегда):
$$
x_1,...,x_n -- \text{выборка}
$$
$$
\xi_1,...,\xi_n -- \text{н.о.р.с.в} ~~\sim F_{\xi},
$$
$$
F_{\xi} \in \{F_{\theta} \}_{\theta \in \Theta}.
$$
Две оценки
$$
\hat{\theta_1}~~\text{и}~~\hat{\theta_2}.
$$
 Допустим, что они обе несмещенные и обе состоятельные. Какая лучше?
 
\end{frame}


\begin{frame}
\frametitle{Функция штрафа}
Рассмотрим разность:
$$
\hat{\theta}_n - \theta,
$$
где $\hat{\theta}_n$ -- оценка, а - $\theta$ -- истинное значение оцениваемого параметра. Сколько мы "заплатим" за неравенство нулю это разности?

~
~
\\
~


Введём некоторую функцию, называемую \textbf{функцией штрафа}  или \textbf{функцией потерь}:
 $$
 U(\cdot)
 $$


\end{frame}


\begin{frame}
\frametitle{Функция штрафа. Предположения.}

\textbf{Функция штрафа}  или \textbf{функция потерь}:
 $$
 U(\cdot)
 $$

Предположения:
\begin{enumerate}
    \item $$
U(0)=0,
$$
\item
$$
U(x)=U(-x) 
$$
- четная функция,
\item
$$
U(x)=U(-x) 
$$
монотонная.
\end{enumerate}




Примеры
$U(x)=x^2$, $U(x)=|x|$.
\end{frame}


\begin{frame}
\frametitle{Функция штрафа (для оценки)}
Естественно  в эту функцию
подставлять разность между оценкой и
неизвестным параметрам
$$
U(\hat{\theta}_n - \theta).
$$
Какой мы штраф заплатим за то, что оценка
ошиблась в какую-либо сторону.

\end{frame}

\begin{frame}
\frametitle{Функция риска}
Какой мы штраф заплатим за то, что оценка
ошиблась в какую-либо сторону.


Функция риска:
$$
\mathcal{R}_{\hat{\theta}_n}(\theta) = \mathrm{\mathbf{E}}U(\hat{\theta}_n - \theta),
$$
аргумент этой функции --  неизвестный параметр, который меняется
в рамках параметрического множества.



Примеры: квадратичная функция риска, или
абсолютная, и т.д.
\end{frame}


\begin{frame}
\frametitle{Функция риска}
Если оценка $\hat{\theta_n}$ --
несмещенная оценка параметра $\theta$, 
(то тогда параметр $\theta$ представляет собою математическое ожидание $\hat{\theta_n}$), 
и 
$$U(x)=x^2, $$

то 
$$
\mathcal{R}_{\hat{\theta}_n}(\theta) = \mathrm{\mathbf{D}}\hat{\theta}_n.
$$
\end{frame}



\begin{frame}{Картинка}

\end{frame}

\begin{frame}{Подходы}
\begin{enumerate}
    \item интегральный
    \item минимаксный
\end{enumerate}

\end{frame}

\begin{frame}{Интегральная оценка}
 $$
\int_{\Theta} \mathcal{R}_{\hat{\theta}_n}(\theta) d \theta 
\to \min_{\hat{\theta}_n}
$$
нас интересует  минимизация этого
интеграла  по
всем $\hat{\theta}_n$. 
\end{frame}

\begin{frame}{Миминимаксный (minimax)}
Минимаксный подход
$$
\max_{\theta \in \Theta} \mathcal{R}_{\hat{\theta}_n}(\theta)
\to \min_{\hat{\theta}_n}.
$$
\end{frame}



\begin{frame}
\frametitle{Пример}
Пусть у нас есть
$$
\xi_i \sim \mathcal{N}(\theta, \theta^2)
$$
Оцениваем параметр $\theta$ и считаем что:
$$
\hat{\theta}_n 
\pause
\in \{\mu_n 
\sum_{i=1}^n \xi_i\}
$$

Возьмем квадратичный риск
\begin{eqnarray*}
u(x)=x^2
\end{eqnarray*}
\end{frame}



\begin{frame}
\frametitle{Пример}
Квадратичная функция риска в нашем конкретном примере
$$
 \mathcal{R}_{\hat{\theta}_n}(\theta) =
 \mathrm{\mathbf{E}} (\mu_n \sum_{i=1}^n \xi_i
 - \theta  )^2
$$
\end{frame}

\begin{frame}
\frametitle{Пример}
\begin{eqnarray*}
 \mathcal{R}_{\hat{\theta}_n}(\theta) =
 \mathrm{\mathbf{E}} (\mu_n \sum_{i=1}^n \xi_i
 - \theta  )^2=
 \pause
 \\
 = \mathrm{\mathbf{E}} 
 \Bigg(\mu_n^2
 \pause
 (  \xi_1^2+...+\xi_n^2 +
 \pause
 \sum_{i \neq j} \xi_i \xi_j)
 \pause
 - 2 \mu_n  \theta   \sum_{i=1}^n \xi_i
 \pause
 + \theta^2
 \Bigg) =
 \pause
 \\
 \bigg/
 \mathrm{\mathbf{E}}\xi_i^2= \mathrm{\mathbf{D}}\xi_i+(\mathrm{\mathbf{E}} \xi_i)^2
 =
 \pause
 2 \theta^2,
 \\
 \sum_{i \neq j} \xi_i \xi_j =\theta^2
 \pause
 \bigg/
 \\
 =\mu_n^2 (2n \theta^2+n(n-1)\theta^2) \pause 
 - 2\mu_n \theta^2 n 
 \pause
 + \theta^2=
 \pause
 \\
 =\theta^2(\mu_n^2 2n - 2\mu_n  n +\mu_n^2n(n-1)+ 1)= \\
 \pause
 \theta^2(n(n+1)\mu_n^2 -2n \mu_n   + 1). 
\end{eqnarray*}
\end{frame}

\begin{frame}
\frametitle{Пример}
Окончательно получаем
\begin{align*}
 \mathcal{R}_{\hat{\theta}_n}(\theta) & =
 \\
 & =
 \theta^2(n(n+1)\mu_n^2 -2n \mu_n   + 1). 
\end{align*}
Квадратичная
функция риска может быть  равномерно минимизирована.
\pause
$$
\frac{2n}{2n(n+1)}=\frac{1}{n+1},
$$
Окончательный ответ:
$$
\mu_n=\frac{1}{n+1}.
$$
\end{frame}
%
\begin{frame}
\frametitle{Упражнение}
\textbf{Упражнение}. Примените минимаксный подход:
 $$
 \xi_i \sim Binom(1,\theta)
$$
$$
 a_n\sum_{i=1}^n+b_n, ~~\Theta=[0,1],
 $$
 $$
 u(x)=x^2.
 $$
\end{frame}

\begin{frame}{Упражнение}
    Минимаксной (имеющей наименьший максимум риска) в схеме Бернулли для квадратичного штрафа
является оценка \textit{Ходжеса—Лемана}:
$$
\hat{\theta}_n
= \overline{x}+
\frac{1}{1+\sqrt{x}}
\bigg(
{\frac{1}{2} - \overline{x}}
\bigg).
$$
\end{frame}
%
\begin{frame}{Задача}
    Разбор некоторых теоретических задач (на доске).
\end{frame}

\begin{frame}{Домашнее задание}
    См. на доске.
\end{frame}
%
%
%
%
%
%
%%
%
%
%
%
%


# References

# Footnotes
