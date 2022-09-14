# flutter-renovate-config

Flutter用 Renovate 共通設定

## 設定内容

### autoMerge

パッケージのバージョン固定は自動でマージする

```json
{
  "pin": {
    "automerge": true
  }
}
```

### ignoreDeps

Firebase のライブラリー郡はRenovate を使って更新しない

```json
{
  "ignoreDeps": [
    "cloud_firestore",
    "firebase_messaging",
    "firebase_remote_config",
    "firebase_crashlytics",
    "firebase_analytics",
    "firebase_core",
    "firebase_dynamic_links",
    "firebase_messaging"
  ]
}
```

### schedule

毎週月曜日10時に依存関係更新のPRを作る

```json
{
  "extends": [
    ":timezone(Asia/Tokyo)"
  ],
  "schedule": [
    "after 10am on Monday"
  ]
}
```