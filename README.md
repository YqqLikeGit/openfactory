# OpenFactory 🏭

**Turn your coding agent into a hardware product development team.**

Skills that teach Claude Code / Codex / Cursor how physical products actually get made —
DFM review, tooling quotes, BOM costing, supplier RFQs, compliance, mass-production ramp.

> Co-written with a real OEM factory owner in Zhejiang, China — the person the world's
> drinkware brands call when they need a product actually manufactured, not rendered.

[English](#why) | [中文](#中文说明)

---

## Why

Your AI can ship software all day. Ask it to take a physical product from idea to a
container leaving a factory, and it starts hallucinating — because almost nobody who
writes on the internet has ever paid for an injection mold, negotiated an MOQ, or failed
a drop test three days before Chinese New Year.

The knowledge in these skills doesn't come from blog posts. It comes from a factory
floor: real rules of thumb about wall thickness and draft angles, how tooling is
actually quoted, what a supplier needs before they'll give you a price that means
anything, and which certification stops your shipment at which border.

**Every number in this repo is a starting-point range, not a quote.** Your geometry,
your volumes, and your supplier's order book set the real price. The skills say so, loudly.

## Skills

| Skill | What your agent learns to do |
|-------|------------------------------|
| [`dfm-check`](skills/dfm-check/SKILL.md) | Review a part design for manufacturability before you pay for steel: walls, draft, ribs, bosses, undercuts, tolerances |
| [`mold-quote`](skills/mold-quote/SKILL.md) | Decode and sanity-check injection-mold quotes: cavity count, steel grade, runner system, T1 timeline, amortization math |
| [`bom-cost`](skills/bom-cost/SKILL.md) | Build a real BOM and cost stack — materials, process, labor, overhead, scrap, margin, landed cost — and work backwards from retail price |
| [`supplier-rfq`](skills/supplier-rfq/SKILL.md) | Write RFQs that get real quotes instead of silence (EN + 中文 templates), read the red flags in the replies |

### Roadmap (in order)

`market-scan` · `id-brief` (industrial-design brief) · `cmf-spec` (color/material/finish) ·
`compliance` (CE/FCC/RoHS/EAC/FDA food-contact) · `packaging-droptest` · `qc-aql`
(inspection plans) · `production-ramp` (T1 → PVT → MP) · `cost-down` · `launch`

## Install

```bash
git clone https://github.com/OWNER/openfactory
mkdir -p ~/.claude/skills
cp -r openfactory/skills/* ~/.claude/skills/
```

Cursor / Codex: point your rules file at the skill you need, or paste its body.
Each skill is self-contained markdown.

## Who this is for

- Software people building their first physical product
- Hardware startups who can't afford a VP of Manufacturing yet
- Makers graduating from 3D prints to injection molding
- Anyone about to wire a five-figure tooling deposit and feeling unsure

---

## 中文说明

**把你的编程助手变成一支硬件产品开发团队。**

这套技能教会 Claude Code / Codex / Cursor 实体产品到底是怎么造出来的：可制造性审查
（DFM）、开模报价拆解、BOM 成本核算、供应商询价、认证合规、量产爬坡。

> 与一位真实的浙江 OEM 工厂老板共同编写——他不是在网上读过制造业，他是天天在车间里
> 给全球品牌把产品真正造出来的人。

为什么需要它：AI 写软件很流利，但你让它把一个实体产品从想法带到集装箱出厂，它就开始
一本正经地胡编——因为互联网上写文章的人，几乎没人真正付过模具钱、谈过 MOQ、或者在
出货前三天摔坏过跌落测试。

**本仓库里所有数字都是"起点参考区间"，不是报价。** 你的结构、你的量、供应商当月的
订单饱和度才决定真实价格——每个技能文件里都会大声重复这句话。

安装方法见上文 Install。每个技能都是独立的 markdown 文件，Claude Code 放进
`~/.claude/skills/`，Cursor/Codex 贴进规则文件即可。

## License

MIT — see [LICENSE](LICENSE). Numbers are educational starting points, not quotations;
always verify with your supplier.
