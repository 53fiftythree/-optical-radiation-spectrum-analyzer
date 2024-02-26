Включенный пример
CCS_Spectrometer
Этот пример показывает, как инициализировать спектрометр CCS100, CCS175 или CCS200. Он устанавливает время интегрирования, измеряет и отображает спектр.

Код использует DLL-файл библиотеки C для спектрометра CCS TLCCS_64.

Чтобы избежать сообщений об ошибках, закомментируйте соглашения о вызове "__fastcall" и "signed" в заголовочном файле "visatype.h" в папке: C:\Program Files\IVI Foundation\VISA\Win64\Include
```C
/*---------------------------------------------------------------------------*/
/* Distributed by IVI Foundation Inc. */
/* */
/* Do not modify the contents of this file. */
/*---------------------------------------------------------------------------*/
/* */
/* Title : VISATYPE.H */
/* Date : 20-12-2023 */
/* Purpose : Fundamental VISA data types and macro definitions */
/* */
/*---------------------------------------------------------------------------*/
#ifndef __VISATYPE_HEADER__
#define __VISATYPE_HEADER__
#if defined(_WIN64)
#define _VI_FAR
#define _VI_FUNC                     //__fastcall
#define _VI_FUNCC                    //__fastcall
#define _VI_FUNCH                    //__fastcall
#define _VI_SIGNED                   //signed
#elif (defined(WIN32) || defined(_WIN32) || defined(__WIN32__) || defined(__NT__)) &&
!defined(_NI_mswin16_)
#define _VI_FAR
.
.
.

```
