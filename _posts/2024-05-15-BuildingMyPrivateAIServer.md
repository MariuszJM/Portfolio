---
layout: post
title:  "Building My Private AI Server"
author: sal
categories: [AI, PC Building,  AI Server]
image: assets/images/ai_server.jpg
comments: false
featured: true

---
Creating a high-performance AI PC within a budget of 8000 to 12000 PLN requires a delicate balance of cost and performance. Therefore to make the process simpler, I decided to consider two setups: one that is budget-friendly yet powerful within the lower range of the budget, and another that pushes the performance limits while staying within the same budget constraints.


The goal was clear: to run large language models (LLMs) such as LLAMA3:8b and potentially LLAMA:70b, fine-tune these remarkable AI models, and achieve a high degree of autonomy, enabling the use of this cutting-edge AI technology even without an internet connection.



## Component Selection Process

The component selection process for my AI PC was driven by a careful evaluation of each item's price-to-value ratio, aiming to achieve the highest overall value to price ratio for the entire system. I started with the big players: the GPU and CPU, the brain and heart of the system. After picking these key components, I moved on to the supporting cast, making sure each part played well with the others to create a smooth and powerful machine.

### GPU Selection

The GPU is the brain of the entire operation, determining the performance in AI-related tasks. I decided it would be the most expensive component, setting the stage for other choices and price configurations.

Based on the official Nvidia site ([Nvidia GeForce Graphics Cards](https://www.nvidia.com/en-us/geforce/graphics-cards/compare/)) and benchmark effective speed ([UserBenchmark GPU Comparison](https://gpu.userbenchmark.com/Compare/Nvidia-RTX-4080-S-Super-vs-Nvidia-RTX-4070-TS-Ti-Super/4156vs4155)), I decided to use the effective speed of the **RTX 4070Ti SUPER** as a reference.

I chose the 40 series GPUs for their better performance and lower energy consumption, which is important for my goal of achieving autonomy or semi-autonomy from electricity.

I considered the following models:

- **RTX 4090**
- **RTX 4080 SUPER**
- **RTX 4070Ti SUPER**
- **RTX 4070 SUPER**
- **RTX 4060Ti SUPER**

These models were available at the store from which I ordered components.

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <th style="border: 1px solid black; padding: 8px;">Model</th>
    <th style="border: 1px solid black; padding: 8px;">CUDA Cores</th>
    <th style="border: 1px solid black; padding: 8px;">Memory</th>
    <th style="border: 1px solid black; padding: 8px;">Power (W)</th>
    <th style="border: 1px solid black; padding: 8px;">Price (PLN)</th>
    <th style="border: 1px solid black; padding: 8px;">Effective Speed (%)</th>
    <th style="border: 1px solid black; padding: 8px;">Effective Speed to Price Ratio (%/PLN)</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">RTX 4090</td>
    <td style="border: 1px solid black; padding: 8px;">16384</td>
    <td style="border: 1px solid black; padding: 8px;">24GB</td>
    <td style="border: 1px solid black; padding: 8px;">450</td>
    <td style="border: 1px solid black; padding: 8px;">8590</td>
    <td style="border: 1px solid black; padding: 8px;">148</td>
    <td style="border: 1px solid black; padding: 8px;">0.017224</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">RTX 4080 SUPER</td>
    <td style="border: 1px solid black; padding: 8px;">10240</td>
    <td style="border: 1px solid black; padding: 8px;">16GB</td>
    <td style="border: 1px solid black; padding: 8px;">320</td>
    <td style="border: 1px solid black; padding: 8px;">4870</td>
    <td style="border: 1px solid black; padding: 8px;">120</td>
    <td style="border: 1px solid black; padding: 8px;">0.024641</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">RTX 4070Ti SUPER</td>
    <td style="border: 1px solid black; padding: 8px;">8448</td>
    <td style="border: 1px solid black; padding: 8px;">16GB</td>
    <td style="border: 1px solid black; padding: 8px;">285</td>
    <td style="border: 1px solid black; padding: 8px;">3990</td>
    <td style="border: 1px solid black; padding: 8px;">100</td>
    <td style="border: 1px solid black; padding: 8px;">0.025063</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">RTX 4070 SUPER</td>
    <td style="border: 1px solid black; padding: 8px;">7168</td>
    <td style="border: 1px solid black; padding: 8px;">12GB</td>
    <td style="border: 1px solid black; padding: 8px;">215</td>
    <td style="border: 1px solid black; padding: 8px;">2999</td>
    <td style="border: 1px solid black; padding: 8px;">80</td>
    <td style="border: 1px solid black; padding: 8px;">0.026676</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">RTX 4060Ti SUPER</td>
    <td style="border: 1px solid black; padding: 8px;">4352</td>
    <td style="border: 1px solid black; padding: 8px;">12GB</td>
    <td style="border: 1px solid black; padding: 8px;">160</td>
    <td style="border: 1px solid black; padding: 8px;">2185</td>
    <td style="border: 1px solid black; padding: 8px;">58</td>
    <td style="border: 1px solid black; padding: 8px;">0.026545</td>
  </tr>
</table>

For the premium setup, I chose the **MSI GeForce RTX 4080 SUPER VENTUS 3X OC 16GB DLSS 3**. The effective speed-to-price ratio for the RTX 4080 SUPER is relatively linear, making it an excellent stopping point for a premium solution. For the budget-friendly setup, I selected the **RTX 4070Ti SUPER**, which offers the best performance in the lower part of the budget range.


### CPU Selection

When it came to choosing a new CPU, my primary focus was on finding the best value for my money. I needed a processor that offered a great balance between performance and cost-effectiveness. This led me to compare two models from AMD's Ryzen 9 series, both of which are known for their impressive capabilities.

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <th style="border: 1px solid black; padding: 8px;">Model</th>
    <th style="border: 1px solid black; padding: 8px;">Clock Speed</th>
    <th style="border: 1px solid black; padding: 8px;">Cores</th>
    <th style="border: 1px solid black; padding: 8px;">Threads</th>
    <th style="border: 1px solid black; padding: 8px;">TDP</th>
    <th style="border: 1px solid black; padding: 8px;">Price (PLN)</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">AMD Ryzen 9 7950X3D</td>
    <td style="border: 1px solid black; padding: 8px;">4.2 GHz (Turbo: 5.7 GHz)</td>
    <td style="border: 1px solid black; padding: 8px;">16</td>
    <td style="border: 1px solid black; padding: 8px;">32</td>
    <td style="border: 1px solid black; padding: 8px;">120W</td>
    <td style="border: 1px solid black; padding: 8px;">2686.58</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">AMD Ryzen 9 7900</td>
    <td style="border: 1px solid black; padding: 8px;">3.7 GHz (Turbo: 5.4 GHz)</td>
    <td style="border: 1px solid black; padding: 8px;">12</td>
    <td style="border: 1px solid black; padding: 8px;">24</td>
    <td style="border: 1px solid black; padding: 8px;">65W</td>
    <td style="border: 1px solid black; padding: 8px;">1702.58</td>
  </tr>
</table>


After extensive deliberation (and a bit of emotional turmoil), I was initially drawn to the Ryzen 9 7950X3D due to its exceptional power, even though it comes with higher power consumption and a steeper price tag. On the other hand, the Ryzen 9 7900 stood out as a highly attractive alternative. Its lower power draw and more affordable price made it an ideal choice for a budget-conscious setup, providing a balanced performance without significant compromises.

### Motherboard Selection

After thorough research, I decided on the Gigabyte B650 EAGLE AX motherboard due to its excellent compatibility and features that matched my specific requirements. This motherboard supports both the AMD Ryzen 9 7950X3D and the AMD Ryzen 9 7900 processors, ensuring optimal performance with either of my chosen CPUs. It is compatible with DDR5 RAM, providing high-speed performance without the need for overclocking, which can sometimes lead to instability. However, it also offers robust overclocking capabilities for those who wish to push their RAM beyond standard speeds, adding flexibility for future performance tuning.

The Gigabyte B650 EAGLE AX comes with built-in Bluetooth, WiFi, and audio, providing essential connectivity and convenience. It includes at least two slots for graphics cards, which is perfect for future upgrades or multi-GPU setups. The presence of USB-C and USB 3.2 ports allows for easy connection to the front panel of the case, enhancing accessibility and usability. Additionally, it offers the capability to add additional hard drives, ensuring ample storage capacity for future needs. The motherboard has received good reviews, adding to my confidence in its reliability and performance.

Given these advantages, I decided to use the same motherboard for both of my PC setups, ensuring consistency and ease of maintenance.

### RAM Selection

RAM capacity and speed are crucial for AI tasks. I opted for the Kingston Fury Beast Black series, as ferocious as its name suggests. For the premium setup, a whopping 64GB of G.Skill Ripjaws S5 [2x32GB 6000MHz DDR5 CL30 XMP3 DIMM] was chosen, perfect for handling large models like LLAMA3:70b (40 GB). The Gigabyte B650 EAGLE AX motherboard can manage speeds up to 5400MHz without overclocking. However, to maximize performance, I decided to use the overclocking feature of the motherboard to achieve higher speeds, even though it could introduce some instability. For the budget setup, 32GB should suffice for smaller models.

### CPU Cooling System Selection

Efficient cooling is essential to maintain performance and prolong component life. For a premium setup, the ENDORFY Navis F360 provides a high-performance liquid cooling solution, keeping your CPU as cool as the other side of the pillow. For a budget setup, the ENDORFY Navis F240 offers a smaller, more cost-effective liquid cooler, ensuring the Ryzen 9 7900 stays frosty.

### Storage Selection

For both setups, I selected the Lexar NM790 PCI-e NVMe 1TB SSD, offering high-speed data transfer and ample storage capacity—because waiting for files to transfer is so 2020. This SSD delivers impressive read speeds of up to 7400 MB/s and write speeds of up to 6500 MB/s, ensuring that my system runs smoothly and efficiently. With its 1TB capacity, it provides plenty of space for all my applications, games, and files, making it an excellent choice for both performance and storage needs.

### Power Supply Selection

When choosing a power supply, stability and efficiency are crucial. For my premium setup, I chose the Corsair RM1000X SHIFT, providing 1000 watts of reliable power. Its 80 PLUS Gold certification ensures high energy efficiency, and fully modular cables keep the build organized, enhancing airflow and thermal performance. Known for its reliability, it's ideal for long-term stability.

For a budget-friendly option, I picked the Gigabyte GP-P850GM. It offers 850 watts of power with 80 PLUS Gold efficiency. Semi-modular cables aid in tidy cable management. With solid reviews, it provides a cost-effective solution without compromising performance.

### Case Selection

The ENDORFY Arx 700 ARGB case was my choice for its spacious design, optimal ventilation with three intake and one exhaust fan, and the ability to add additional fans - because nobody likes a stuffy case.

## Overall Price and Value Comparison

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <th style="border: 1px solid black; padding: 8px;">Component</th>
    <th style="border: 1px solid black; padding: 8px;">Budget Setup (PLN)</th>
    <th style="border: 1px solid black; padding: 8px;">Premium Setup (PLN)</th>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Processor</td>
    <td style="border: 1px solid black; padding: 8px;">1702.58</td>
    <td style="border: 1px solid black; padding: 8px;">2686.58</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">GPU</td>
    <td style="border: 1px solid black; padding: 8px;">3990.96</td>
    <td style="border: 1px solid black; padding: 8px;">4870.18</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Motherboard</td>
    <td style="border: 1px solid black; padding: 8px;">739</td>
    <td style="border: 1px solid black; padding: 8px;">739</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">RAM</td>
    <td style="border: 1px solid black; padding: 8px;">488.85</td>
    <td style="border: 1px solid black; padding: 8px;">917.52</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Cooling</td>
    <td style="border: 1px solid black; padding: 8px;">349</td>
    <td style="border: 1px solid black; padding: 8px;">513.17</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Storage</td>
    <td style="border: 1px solid black; padding: 8px;">357.07</td>
    <td style="border: 1px solid black; padding: 8px;">357.07</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Power Supply</td>
    <td style="border: 1px solid black; padding: 8px;">399.07</td>
    <td style="border: 1px solid black; padding: 8px;">559</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Case</td>
    <td style="border: 1px solid black; padding: 8px;">552.50</td>
    <td style="border: 1px solid black; padding: 8px;">552.50</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px; font-weight: bold;">Total</td>
    <td style="border: 1px solid black; padding: 8px; font-weight: bold;">8,579.03</td>
    <td style="border: 1px solid black; padding: 8px; font-weight: bold;">11,195.02</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">GPU - Effective Speed (%)</td>
    <td style="border: 1px solid black; padding: 8px;">100</td>
    <td style="border: 1px solid black; padding: 8px;">120</td>
  </tr>
  <tr>
    <td style="border: 1px solid black; padding: 8px;">Speed/Price Ratio</td>
    <td style="border: 1px solid black; padding: 8px;">0.01166</td>
    <td style="border: 1px solid black; padding: 8px;">0.01072</td>
  </tr>

</table>

While the budget setup boasts a slightly better speed-to-price ratio, the premium setup excels in overall performance. The premium setup's RTX 4080 SUPER delivers a substantial performance boost for a reasonable price increase, making it the top pick for demanding AI tasks. Though the decision wasn't easy, the phrase "go big or go home" ultimately convinced me to choose the premium option.


## Performance Evaluation of the Chosen Setup

To thoroughly evaluate the performance of my premium setup, I conducted benchmarking using Open Web UI to measure the tokens per second for various AI models.

Specifically, I tested the premium setup equipped with an RTX 4080 Super and achieved a generation speed of 82 tokens per second for the LLAMA2:7b model. This result is notably impressive, surpassing the performance reported in a  [YouTube](https://www.youtube.com/watch?v=Ugp6wKio1eE) video, where an Intel Core i9-13900K paired with an RTX 4090 achieved a speed of 75 tokens per second. This benchmark demonstrates the exceptional efficiency and capability of my chosen components, reinforcing the value of my configuration choices.

## Conclusion

Building a high-performance AI PC within a budget of 8000 to 12000 PLN required balancing cost and performance. I considered two setups: a budget-friendly option and a premium option, both designed to run large language models (LLMs) like LLAMA3:8b and LLAMA:70b.

The GPU was the key component, and I chose the RTX 4080 SUPER for the premium setup and the RTX 4070Ti SUPER for the budget-friendly setup. For the CPU, I compared two AMD Ryzen 9 models: the Ryzen 9 7950X3D for the premium setup and the Ryzen 9 7900 for the budget setup. The Gigabyte B650 EAGLE AX motherboard was selected for its compatibility with both CPUs, support for DDR5 RAM, built-in Bluetooth, WiFi, audio, and ample expansion options. The premium setup featured 64GB of G.Skill Ripjaws S5 RAM, while the budget setup had 32GB of Kingston Fury Beast RAM. Efficient cooling was ensured with the ENDORFY Navis F360 for the premium setup and the ENDORFY Navis F240 for the budget setup. The Lexar NM790 PCI-e NVMe 1TB SSD was chosen for its high-speed data transfer and ample storage capacity. The Corsair RM1000X SHIFT was selected for the premium setup, while the Gigabyte GP-P850GM was chosen for the budget-friendly option. The ENDORFY Arx 700 ARGB case was selected for its spacious design and optimal ventilation. The total cost for the premium setup was 11,195.02 PLN, while the budget setup totaled 8,579.03 PLN. Ultimately, I opted for the premium setup for its superior performance.

Benchmarking showed the premium setup, with an RTX 4080 Super, achieved a generation speed of 82 tokens per second for the LLAMA2:7b model, surpassing a setup featuring an Intel Core i9-13900K and RTX 4090 at 75 tokens per second. This demonstrated the efficiency and capability of my chosen components.

In summary, my AI PC build within the 8000 to 12000 PLN budget successfully balanced cost and performance, resulting in a powerful and efficient setup capable of autonomously running and fine-tuning large language models.