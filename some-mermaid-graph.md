# Some mermaid graph

```mermaid
  graph TD;
      A-->B;
      A-->C;
      B-->D;
      C-->D;
```

Good?

## Graph 2

```mermaid
  graph TD
      graham-- 10G ---graham
      graham-- 10G ---bill
      graham-- 100G ---astrid
      graham-- 1G ---bill
      graham-- 10G ---graham
      graham-- 1G ---Arista
      click astrid "https://github.com/ackxolotl/doctor-cluster-config/blob/mermaid/docs/tum/astrid.md" "astrid"
      click bill "https://github.com/ackxolotl/doctor-cluster-config/blob/mermaid/docs/tum/bill.md" "bill"
```

## Graph 3

```mermaid
  graph TD
    c1-->a2
    subgraph graham
    a1-->a2
    end
    subgraph bill
    b1-->b2
    end
    subgraph astrid
    c1-->c2
    end
```

## Graph 4

```mermaid
  graph TD
    enp2s0f0np0-- 1G ---D["nz-srvr2s2.informatik.tu-muenchen.de"]
    enp196s0f0np0-- 10G ---bill
    enp196s0f1np1-- 10G ---astrid
    subgraph graham
    graham.something["eno1"]
    enp2s0f0np0
    enp196s0f1np1
    enp196s0f0np0
    end
    click astrid "https://github.com/ackxolotl/doctor-cluster-config/blob/mermaid/docs/tum/astrid.md" "astrid"
    click bill "https://github.com/ackxolotl/doctor-cluster-config/blob/mermaid/docs/tum/bill.md" "bill"
```

## Graph 5

```mermaid
  graph TD
    graham.enp2s0f0np0["enp2s0f0np0"]-- 10G ---outside
    graham.enp196s0f0np0["enp196s0f0np0"]-- 10G ---graham.enp2s0f0np0["enp2s0f0np0"]
    graham.enp196s0f0np0["enp196s0f0np0"]-- 10G ---graham.enp196s0f1np1["enp196s0f1np1"]
    graham.enp196s0f1np1["enp196s0f1np1"]-- 10G ---graham.enp2s0f0np0["enp2s0f0np0"]
    graham.enp196s0f1np1["enp196s0f1np1"]-- 10G ---graham.enp196s0f0np0["enp196s0f0np0"]
    subgraph grahamster
    graham.enp2s0f0np0["enp2s0f0np0"]
    graham.enp196s0f0np0["enp196s0f0np0"]
    graham.enp196s0f0np0["enp196s0f0np0"]
    graham.enp196s0f1np1["enp196s0f1np1"]
    graham.enp196s0f1np1["enp196s0f1np1"]
    end
    click outside "https://nz-srvr2s2.informatik.tu-muenchen.de/" "outside"
```
