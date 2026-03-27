# images/

將自定義圖片放入此資料夾，然後在 `index.html` 的 `ASSETS` 區塊取消對應的注釋即可生效。

---

## 檔案命名規範

### 背景圖片
| 檔名 | 對應場景 |
|------|----------|
| `bg_home.jpg` | 主角家（深夜電腦前） |
| `bg_shop.jpg` | 網路賣家頁面 |
| `bg_living.jpg` | 主角客廳 |
| `bg_vet.jpg` | 動物醫院 |
| `bg_police.jpg` | 警察局 |
| `bg_court.jpg` | 法庭 |
| `bg_dark.jpg` | 暗場過渡 |
| `bg_ending.jpg` | 結局背景 |

建議尺寸：**900 × 600 px**，格式 `.jpg` 或 `.png`

---

### 人物立繪（透明背景 PNG）

#### 主角 雨晴
| 檔名 | 表情 |
|------|------|
| `player_normal.png` | 一般 |
| `player_happy.png` | 開心 |
| `player_sad.png` | 難過 |
| `player_angry.png` | 憤怒 |
| `player_determined.png` | 堅定 |

#### 反派 林詐欺
| 檔名 | 表情 |
|------|------|
| `seller_sly.png` | 油滑 |
| `seller_scared.png` | 害怕 |

#### 配角
| 檔名 | 角色 |
|------|------|
| `vet.png` | 王獸醫 |
| `police.png` | 陳警官 |

建議尺寸：**200 × 340 px**，格式 `.png`（需透明背景）

---

### 貓咪
| 檔名 | 狀態 |
|------|------|
| `cat_sick.png` | 生病（初登場） |
| `cat_healthy.png` | 健康（結局） |

建議尺寸：**120 × 120 px**，格式 `.png`（需透明背景）

---

## 使用方式

上傳圖片後，打開 `index.html` 找到 `ASSETS` 區塊，把對應行的 `//` 移除：

```js
const ASSETS = {
  backgrounds: {
    home: 'images/bg_home.jpg',      // ← 移除 // 後生效
  },
  characters: {
    player: {
      normal: 'images/player_normal.png',
    },
  },
  cat: {
    sick: 'images/cat_sick.png',
  },
};
```

未填入的項目會自動使用內建 SVG／漸層，不影響其他項目。
