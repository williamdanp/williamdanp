### Hi, I'm Daniel William

Systems and low-level engineer. I take the problems people call impossible
and keep pushing until the hardware gives in. I also build backends and
production network tooling that has to stay up.

I run [Haxall Tech](https://haxalltech.com.br): 50+ software and
infrastructure projects delivered.

---

#### Two NVIDIA drivers, two GPUs, one machine

I got a 2012 GTX 650 and a modern GTX 1660 Super running at the same time,
each on a different NVIDIA driver version, two branches that normally refuse
to coexist.

First on Windows, the harder one: I edited the driver's own call paths so the
470 branch driving the 650 would not collide with the newer branch driving the
1660 Super, then wrote a shim that stands in for nvapi.dll and nvapi64.dll and
routes telemetry and control across both cards at once.

Then on Linux, for other reasons, I rebuilt the idea from scratch: a Vulkan 1.3
emulation layer in C (dynamic rendering, a residency pager) that lets a Kepler
card run software it was never meant to, plus a Rust daemon and a live desktop
widget watching both GPUs. It got far enough to launch CS2 (Counter-Strike 2)
on a card NVIDIA and Valve both treat as unsupported.

Rust, C, Vulkan, driver-level patching, sparse binding, PCIe P2P.

---

#### Self-healing monitoring for a regional ISP

In-house monitoring and remediation for a wireless ISP (500+ subscribers), no
Zabbix and no Grafana, all my own:

- Multi-protocol telemetry: SNMP, ICMP, router APIs and RF spectrum scans
- Active RF channel remediation, chosen from interference data cross-referenced by time of day and weekday
- An auto-revert dead-man's switch: any change that fails, degrades a link, or goes unconfirmed is undone by the device itself, so a bad change can never brick a tower
- Proven against the real router OS running virtualized, 19 of 19 on every firmware branch in the fleet

Python, PostgreSQL, Docker, SNMP, custom RF analytics.

---

#### Building now (private)

An operating system for a company run by AI agents: broad autonomy on the safe
work, and every irreversible action stopped at a human gate by design. Most of
the effort is the safety engineering, built test-first and put through
adversarial red-teaming. Details on request.

---

#### Shipped and live

| Project | What it is | Stack |
|---|---|---|
| [Parcelu](https://parcelu.com.br) | Installment and expense tracking SaaS | FastAPI, PostgreSQL, Docker, React |
| [Dr. h.c. Alef Sigma](https://drhcalefsigma.com.br) | Handcrafted copper e-commerce | WooCommerce, PHP, Correios API |

---

#### Stack

`Rust` `C` `Python` `FastAPI` `C#` `PostgreSQL` `Docker` `React` `Linux` `MikroTik` `SNMP`

Systems Analysis and Development, postgraduate in Software Engineering and
Information Security, 10+ years in IT and networking.

---

[haxalltech.com.br](https://haxalltech.com.br) · [LinkedIn](https://www.linkedin.com/in/williamdanp) · haxalltech@gmail.com
