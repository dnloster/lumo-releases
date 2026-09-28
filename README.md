# Lumo Releases (public)

Repo **public** chỉ chứa thông tin cập nhật + APK.
Source code nằm ở repo private `lumo-mobile`.

## Cấu trúc

- `update.json` — manifest app đọc khi mở
- GitHub **Releases** — đính kèm file `lumo-release.apk`

## App đang trỏ tới

```
https://raw.githubusercontent.com/dnloster/lumo-releases/main/update.json
```

## Phát hành bản mới

1. Trong `lumo-mobile`: tăng `version` + `android.versionCode` trong `app.json`, build APK.
2. Tạo GitHub Release tag `vX.Y.Z`, upload `lumo-release.apk`.
3. Sửa `update.json`:

```json
{
  "versionCode": 3,
  "versionName": "1.2.0",
  "apkUrl": "https://github.com/dnloster/lumo-releases/releases/download/v1.2.0/lumo-release.apk",
  "notes": "- Nội dung cập nhật",
  "forceUpdate": false
}
```

4. Commit + push `update.json` lên `main`.
