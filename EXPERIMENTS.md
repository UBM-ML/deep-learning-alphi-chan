# Experiment Log

Catat setiap percobaan hyperparameter di sini. **Minimal 5 eksperimen.**

> Tips: ubah **satu hyperparameter pada satu waktu** agar bisa mengisolasi efeknya. Setelah memahami efek tiap variabel, baru gabungkan untuk hasil terbaik.

---

## 📋 Tabel Ringkasan

Isi tabel ini setelah selesai semua eksperimen.

| # | Hidden | Neurons | Activation | Optimizer | LR     | Batch | Epochs | Dropout | Test Acc | Train Time |
|---|--------|---------|------------|-----------|--------|-------|--------|---------|----------|------------|
| 0 | 1      | 64      | relu       | sgd       | 0.01   | 32    | 10     | 0.0     | ~85%     | ~30s       |
| 1 | 2      | 256     | relu       | adam      | 0.001  | 128   | 50     | 0.3     |  ~89%    | 71.4s      |
| 2 | 3      | 128     | relu       | adam      | 0.001  | 32    | 20     | 0.3     |  87.77%  |  108.7     |
| 3 | 4      | 256     | relu       | adam      | 0.001  | 64    | 40     | 0.2     |  89.07%  |   118.9s   |
| 4 |        |         |            |           |        |       |        |         |          |            |
| 5 |        |         |            |           |        |       |        |         |          |            |

> **Eksperimen #0** = baseline (jangan ubah, ini patokan kalian).

---

## 🧪 Detail Setiap Eksperimen

Gunakan template di bawah untuk SETIAP eksperimen.

---

### Eksperimen #1

**Apa yang diubah dari baseline:**
> Contoh: Mengganti optimizer dari `sgd` → `adam`, sisanya tetap.

**Hipotesis sebelum run:**
> Contoh: Adam adalah optimizer adaptif, kami menduga konvergensi akan lebih cepat dan akurasi naik.

**Hasil:**
- Test accuracy: ___%
- Train accuracy: ___%
- Validation accuracy: ___%
- Train time: ___ detik
- Apakah overfit/underfit? ___

**Observasi & Insight:**
>

**Rencana eksperimen berikutnya:**
>

---

### Eksperimen #2

**Apa yang diubah:**

**Hipotesis:**

**Hasil:**  
- Test accuracy: ___%
- Train accuracy: ___%
- Validation accuracy: ___%
- Train time: ___ detik
- Apakah overfit/underfit? ___

**Observasi:**

---

### Eksperimen #3

**Apa yang diubah: mengganti batch, epochs, dan dropout**

**Hipotesis:**

**Hasil:**  
- Test accuracy: 89.07%
- Train accuracy: 91.90%
- Validation accuracy: 90.07%
- Train time: 118.9 detik
- Apakah overfit/underfit? ___

**Observasi:**

---

### Eksperimen #4

**Apa yang diubah:**

**Hipotesis:**

**Hasil:**  
- Test accuracy: ___%
- Train accuracy: ___%
- Validation accuracy: ___%
- Train time: ___ detik
- Apakah overfit/underfit? ___

**Observasi:**

---

### Eksperimen #5

**Apa yang diubah:**

**Hipotesis:**

**Hasil:**  
- Test accuracy: ___%
- Train accuracy: ___%
- Validation accuracy: ___%
- Train time: ___ detik
- Apakah overfit/underfit? ___

**Observasi:**

---

## 🏆 Konfigurasi Terbaik

Setelah semua eksperimen, salin konfigurasi terbaik kalian ke sini:

```python
HIDDEN_LAYERS     = ?
NEURONS_PER_LAYER = ?
ACTIVATION        = ?
DROPOUT_RATE      = ?
OPTIMIZER         = ?
LEARNING_RATE     = ?
BATCH_SIZE        = ?
EPOCHS            = ?
```

**Test accuracy final: ___%**
