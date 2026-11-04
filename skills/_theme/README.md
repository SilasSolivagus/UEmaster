# 主题包

给 flow-canvas / flow-walkthrough 用的配色覆盖，来源于 `roxorlt/ui-design` 的设计变量。

| 文件 | 对应规范 | 用途 |
| --- | --- | --- |
| `rquant-light.style.json` | rQuant v1.3.1（浅色） | 默认。评审、打印、投影 |
| `mdt-dark.style.json` | 门店通 v1.0（深色） | 深色场景，OLED 屏 |

用法：

```bash
python3 skills/flow-canvas/scripts/flowlayout.py in.mmd -o out.svg --style skills/_theme/rquant-light.style.json
```

flow-walkthrough 的主题在 walkmap 的 `css_vars` 里，见下方对照。

## 变量对照

| walkmap css_vars | rQuant light | 门店通 dark |
| --- | --- | --- |
| `--wt-bg` | `#F3F5F7` | `#000000` |
| `--wt-white` | `#FFFFFF` | `#141416` |
| `--wt-border-light` | `#E3E7EC` | `#2C2C31` |
| `--wt-border` | `#CCD3DB` | `#3A3A41` |
| `--wt-text` | `#161A21` | `#F2F2F4` |
| `--wt-dim` | `#5E6776` | `#A1A1AA` |
| `--wt-light` | `#8A92A0` | `#8B8B95` |
| `--wt-fill` | `#ECEFF2` | `#1F1F23` |
| `--wt-accent` | `#2448D0` | `#F5A524` |

## 已知约束

门店通规范写明主色黑色、默认深色，`light` 组是浅色备选、正式产品不用。引入深色主题时沿用其 `dark` 组。

rQuant 是 A 股语境，`up` 用红、`down` 用绿，与通用语义相反。本主题包里 `p0` 取 `crit`（红）、`p1` 取 `warn`（棕黄），不受涨跌色影响。
