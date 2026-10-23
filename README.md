# api-specs

Repositori terpusat untuk seluruh spesifikasi kontrak OpenAPI proyek Gumpalan.

## Struktur

```
api-specs/
├── auth/
│   └── v1/
│       └── openapi.yaml
├── iot/
│   └── v1/
│       └── openapi.yaml
└── README.md
```

## Konvensi Versi

- Jalur spesifikasi mengikuti format: `<service>/<versi>/openapi.yaml`.
- Perubahan non-breaking (field opsional baru, endpoint baru) tetap pada `v1`.
- Perubahan breaking (penghapusan field, perubahan format tipe data, perubahan skema autentikasi) menaikkan versi direktori ke `v2`.

## Menghasilkan Klien Dart

Dapat menggunakan `openapi-generator-cli`:

```bash
# Contoh untuk auth
openapi-generator-cli generate \
  -i auth/v1/openapi.yaml \
  -g dart-dio \
  -o ../app-core-api/lib/src/generated/auth

# Contoh untuk iot
openapi-generator-cli generate \
  -i iot/v1/openapi.yaml \
  -g dart-dio \
  -o ../app-mod-iot/lib/src/generated/iot
```

## Lisensi dan Dependensi

Lisensi repositori ini belum ditentukan. Repositori ini tidak memiliki dependensi pustaka runtime.
