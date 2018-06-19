# Deep learning Hardware
how to choose wisely your computer

##Table of content:
- [I'm a beginner / I'm a student](https://github.com/MelAbgrall/HardwareforAI#im-a-beginner--im-a-student)
- [Laptop vs Cloud vs Prebuilt vs Homemade](https://github.com/MelAbgrall/HardwareforAI#laptop-vs-cloud-vs-prebuilt-vs-homemade)
	- [Laptops](https://github.com/MelAbgrall/HardwareforAI#pro-and-con-of-beefy-laptop)
	- [Cloud computing](https://github.com/MelAbgrall/HardwareforAI#cloud-computing)
	- [Prebuilt](https://github.com/MelAbgrall/HardwareforAI#prebuilt)
	- [Homemade](https://github.com/MelAbgrall/HardwareforAI#homemade)
- [The bottom-up approach: What kind of harware exist, and how to choose it](https://github.com/MelAbgrall/HardwareforAI#the-bottom-up-approach-what-kind-of-harware-exist-and-how-to-choose-it)
	- [Why GPU are so efficient ?](https://github.com/MelAbgrall/HardwareforAI#why-gpu-are-so-efficient-)
	- [Choosing a GPU](https://github.com/MelAbgrall/HardwareforAI#choosing-a-gpu)
	- [Choosing a CPU](https://github.com/MelAbgrall/HardwareforAI#choosing-a-cpu)
	- [Choosing a motherboard](https://github.com/MelAbgrall/HardwareforAI#choosing-a-motherboard)
	- [RAM](https://github.com/MelAbgrall/HardwareforAI#ram)
	- [Storage](https://github.com/MelAbgrall/HardwareforAI#storage)
	- [Cooling the beast](https://github.com/MelAbgrall/HardwareforAI#cooling-the-beast)
	- [Power Supply](https://github.com/MelAbgrall/HardwareforAI#psu)
	- [LEDS](https://github.com/MelAbgrall/HardwareforAI#led)
	- [Fans](https://github.com/MelAbgrall/HardwareforAI#fan)
	- [Case](https://github.com/MelAbgrall/HardwareforAI#case)
	- [Perifericals](https://github.com/MelAbgrall/HardwareforAI#periphericals)
	- [OS](https://github.com/MelAbgrall/HardwareforAI#os)
- [Youtubers to follow & Useful links](https://github.com/MelAbgrall/HardwareforAI#youtubers-to-follow--useful-links)
	

## "I'm a beginner" / "I'm a student"
you dont need a powerful computer (unless you're a gamer).

There is plenty of cloud based solutions that will offer free computing power for a limited time. And even when you are out of free options, it is still a viable option.

If you are learning computer science (and not AI especially), it is better to have a powerful laptop with at least an i5 and integrated gpu. It will allow you to do some small program without the need of bigger machines

## Laptop vs Cloud vs Prebuilt vs Homemade
Before going any further, here is how I'm working with AI:

- I have a small laptop with enough power to do some small computation or small software (like websites for example). It's a thinkpad x230 under Fedora, and it serve me well since 2012, it's ultra light and very small, and I'm not planning to change it anytime soon.

- I have also a small tower with a beefy gpu (1080ti) for heavy computation, photoshop and gaming. I'm planning to upgrade it during summer 2018 for a dual gpu watercooled system. It's running dual boot with windows, and Fedora.

When I'm not on my big computer, I'm using SSHFS and tunels to work. It's easy to set up and it can replace easily cloud options.

#### Pro and con of beefy laptop
Saddly, a lot of people out here recommand to get a gaming laptop for AI.

From personal experience, it is already a somewhat bad choice for gaming, so do not expect to do heavy computation on those laptop !

why ? If you did some thermal / energy engineering, you should probably know about the things I'll talk here

When you are running heavy computation (Games, AI, video rendering, etc) you are using a lot of power. Since our world is not perfect, while doing this you loose some power in form of heat (in electronics it's called TDP and it's in Watt)

So, when you have a laptop, your "cooling potential" aka the size of the heat exchanger / Radiator is small. Thus your laptop fans will need to run full speed to dissipate this heat. And even at full speed, it's not really efficient.

Pro:
- If you don't have internet, you can still work on AI
- After cloud computing, Tight budget friendly

Con:
- Really short lifespan (due to overheat, and smaller component)
- During training, you won't do favors to the battery, either because it's plugged for several hours, or because it's drawing a massive amount of power
- Thermal overload (your computer will slow down to not literally burn, thus longer training time)
- Really noisy
- you can't upgrade it
- Not the most performant / $

#### Cloud computing
Cloud computing is a good option if you don't have a budget or if you are not serious about AI. However, in the long run it's very expensive, so if you are using it daily, see the next two parts


#### Prebuilt
Those computer are very powerful usually. There is two type of prebuilts: the ones by big companies (Asus, MSI, etc) and the ones built by smaller professionals

Prebuilds from big companies share con with beefy laptop

Other prebuild can really worth it, however you need to pay for the guys who will build it, and sometimes you can't go with some particular options.

#### Homemade
The best option out here. You will put only what you need on your computer, this will allow a very wise usage of your money.

For those afraid of building a computer: it's not difficult (12yo children can do it, so you probably can), and it's not very time consuming (you need to plan maximum a week end, and minimum an afternoon)

Pro:
- Only what you need
- You can upgrade it as hardware is evolving (you only need to change a few parts, and keep 90% of your initial build)
- Depending the harware, it can be silent, or extremely silent
- It's very efficient, because you will never have thermal overload.
- You can make a VERY powerful computer (aka 8 GPU)

Con:
- It's very heavy
- It's big
- Your electric bill might explode if you're planning an ultimate 8 gpu build (I can reassure you, for a normal sized computer like 1 / 2 gpu, it's no more than a beefy laptop)
- It's more efficient than a vacuum cleaner, so you need some cleanup roughly every 3 months (it's not mandatory, but you can loose performance if it's too dusty)

when you are using a homemade setup, if you are outside, you only need an internet connection and a small laptop to connect to it. You may even not need to buy a new laptop because you are probably reading this on a portable "computer" (aka something with a keyboard is enough).
Even a chromebook will be suffisient to work.

If you really want to buy a new laptop, there is very good linux laptops out here, Clevo notebooks are really worth it (the original AlienWare were build with Clevo notebooks), and some revendors like System 76 in the US are supporting linux

## The bottom-up approach: What kind of harware exist, and how to choose it
To build a computer you will need at least a motherboard, a cpu, Ram, and stockage (HDD / SSD / M2).
Some CPU (intel primarily) have integrated graphics. It's a very weak gpu, but it's enough for rendering a desktop environment and basic applications (Office, internet, etc)

### Why GPU are so efficient ?
GPU is a specialized piece of hardware (back in the old days, every piece of a computer were plugable, so you could design a good computer by putting less or more card, like Lan card, sound card, etc. This is still the case today)

GPU are not really efficient for all tasks: if you need heavy computation, or a state machine with instructions that depends from the result of previous ones, CPU are still more efficient.
GPU are somewhat good to do basic calculation.
When you take ONE GPU core, it's much slower than a CPU core.
However the incredible power of a GPU is there is a lot of core. So when you have a problem that can be parralelized (example render pixels) they are much more efficient than CPU.
Deep learning tasks can be parralelized, this is why you need a GPU

If you want an example: I did a training with my old x230 on MNIST. Since this laptop don't have a discrete GPU (aka a gpu separated from the CPU) it took nearly 3 day.
On my big computer, it took 5 minutes

### Choosing a GPU
When you are building a deep learning focused computer, the main concern is the gpu, how many ? how efficient ?

3 things are important in a gpu:
- Memory: Less memory mean either smaller batch, or only one model at a time
- Cores: more core = more efficient
- Clock speed: more clock speed = more efficient

**number of gpu > memory > cores > clock**

Depending on the size of your datasets, you can either go with one beefy gpu or two smaller ones (or if you can afford it, two big gpu)
Training multiple model at the same time depend of your data.

For example, with a titan Xp (12GB) you can train 5 Cifar datasets at the same time.

some simple math to estimate roughly your gpu memory need: Batch size(int) * image size(KB/MB) = more or less the ram needed during training

Also note that previous generation hardware (ex 980ti) are also a good value, and still efficient

If you are choosing between Nvidia and AMD, at the moment, Nvidia is much more advanced on AI than AMD, so there is no doubt: go for Nvidia

Last note on GPUs:
Going for 1 or 2 gpu is okay, if you plan to put more than 2 gpu, it will cost you much more to run it (explaination on the next part)

### Choosing a CPU
Choosing a cpu for AI is not the same as choosing a cpu for gaming.

When you are gaming, GPU performances are bounded to the CPU ability since a lot of work is done on the CPU. When you use a less efficient cpu: the gpu is waiting for cpu instructions

Since AI don't need the same computation, you do not have the issue of bottleneking. I still recommand at least an i5 / Ryzen 5 / equivalent

How is CPU used in AI ? Usually the CPU is used for data augmentation before sending it to the GPU.
In the deep learning case, the slower part of the software is the training, and it's happening on the GPU. Since even the best GPU will not train as fast as a CPU can do data augmentation, you will never experience Bottleneking.

#### the generation
You should check first the generation of the cpu: newer cpu are more power efficient than older ones, this mean reducing the electric bill, and increase performances. Be carefull i7 i5 Ryzen 5 / 7 is not the generation, it is the performance indicator.
	example:
- i7 7700 is generation 7
- i5 8600 is generation 8

the performance scale is as follow:
	
	lesser cpu (celeron, etc) < i3 / Ryzen 3 < i5 / Ryzen 5 < i7 / Ryzen 7 < i9 / Threadripper
	
Intel Xeon and AMD Athlon are special kind of cpu, usually not affordable and reserved for datacenter (lot of core, but not very fast)

#### PCIE Lanes
the number of pcie lanes. Usually CPU (5 & 7 series) will come with 16 lanes. pcie lanes are the communication pipes between the cpu and the gpu. A GPU will take maximum 16 lanes, and (for CUDA based application) minimum 8 lanes.

Having only 16 lanes, those gpu need to divide them between the two gpu if you have two. This mean a 10% decrease in performance. **It is not an issue**. 

If you need to plug more gpus, you need more lanes. Be carefull though, splitting lanes is not even (for example the i7 X serie have 28 lanes. However it is splitted in 16x 8x 4x, so you won't be able to put a third GPU) Usually the only CPUs allowing enough lanes for 3+ GPUs are i9 / Threadripper. However it is nearly twice the price of an i7 and the motherboard you will need is also more expensive.
if you need 4+ gpu, there is still a way to do it using Xeon / Athlon processors. Motherboards that are compatible with those cpus are also able to fit two cpu. However, this come at a very high price (it seems however that used datacenter hardware is more affordable)

#### Overclocking
some CPU are overclockable.
This is a special feature for gamers: it allow overclocking your cpu. However this is a really bad idea in computation since this increase chances to have bit errors. **It's a no no.**

in gaming this is not an issue, because bit errors are not visible.

so this little feature is not really useful, you will pay for it.
on intel platform it's marked with a k at the end of the product name (i7 7700k for example)

If you still want an overclockable cpu: it won't harm your computation if you don't overclock it. And you can benefit from higher factory clock speed.
	
Note however:
overclockable 5 series are still physically less powerful than 7 series. So mind the price, sometime it's the same to buy an i5 k and a regular i7, the latest being more powerful.


### Choosing a motherboard
In the past, motherboards quality was very important. This is no longer the case. You still need to check some things

#### compatibility
**The most important part of choosing a motherboard:**

the cpu previously choosen has something called a "socket". And motherboard have also something called a "Chipset"

Basically the chipset is the second heart of a computer, helping the CPU for connecting with your hardware.

The socket is the way of connecting your CPU to the motherboard.

so you need to be very careful: some chipset (ex: 270 & 260) have the same socket (lga 1151) but they won't be compatible with their respective CPU
(by memory, 270 is for 7 gen intel CPU, and 260 for 6th gen)

Don't worry, you can easily find the compatibility (CPU vendors are listing the compatible socket & chipset)

mind also pc configurators that are warning "this cpu is ok, but you need a bios update"
you need two cpu for a bios update and it's kind of complicated.

#### The chipset
so, as seen on the previous point, chipset are important. There is 3 category of chipset: B, H and Z.

This is the "premium features".

a B chipset will be ok to run a machine, the H will add a little bit more functionalities.

The Z chipset is useful for oveclocking. It also has some more features, so usually you don't need it. *and please, do not buy a Z chipset and an i5... it's like buying a Ferrari and replacing the motor by a bicycle.*

#### I/O
check how many sata port you can have on a motherboard (more sata port = more hdd / ssd)

Check also the fan connectors: there is two type of fan, pwm (4 pin) and normal (3 pin). There is no difference between them, but they are not compatible (you can't pin a pwm on a 3 pin, and if you put a 3 pin fan on pwm, it will go full speed)
If the motherboard don't have enough fan pin, don't worry, there is splitters available on internet for a really good price (2 / 5 $)

Check the supported usb version (usb 2.0, 3.0 or 3.1) it will allow you to connect the front usb (on the front of the case)

at last, if you have no other choice than using wifi for the computer, check that the motherboard have wifi integrated, or else you will need to buy a separate expansion card or a dongle

#### note on chipset lanes
The pcie lanes of a chipset on a motherboard are not the same as the ones from the cpu. Do not sum them, it won't work.


#### Size:
2 main types of motherboard size exist: ATX and micro ATX (E-ATX also, but not seen very often)

I do not recommand micro ITX motherboard, they are more expensive and difficult to upgrade

### RAM
Ram is one important piece. *The minimum* Ram you should take is the same as your GPU: you need to put your dataset batch in the ram before sending it to the gpu.
*The recommanded* amount of ram is the sum of the memory on your GPUs

for example:
Titan Xp *2: (12GB effective memory)
	- minimum: 16 GB of ram (12GB sticks doesn't exists)
	- recommanded: 32 GB (same here, 24GB sticks does not exists)
	
Current Ram prices are crazy (there is at the moment a lawsuit against manufacturers about prices agreement between them). So this is understandable to not go for the 32 GB. You can also want to upgrade your computer later... Motherboard have at least 2 places to put ram, so it's always a good move to only take half of the available ram slot, in order to be able to upgrade later.

Check at last their frequency: some ram can go really fast (3200Hz +) but the downside is that it's not supported by the motherboard (as for the CPU, you can easily find the maximum ram speed for every motherboard on the specs / datasheet)

At last, for compatibility, there is currently 4 generation or RAM, DDR1, 2, 3 and DDR4. **They are not backward compatible**

### Storage
So, now you need some storage.
There is 3 main type of storage, with different speed:
HDD (hard disk drive) < SSD (solid state drive) < M2 (ss2 connected with motherboard pcie lanes)

this is fun, because the price is the same.

the recommandation is:

- if you're on a tight budget, forget about SSD and M2. Linux is suffisiently optimized to be faster than windows on HDD.

- If you have a little bit more money you can buy a SSD, but it's around 3 times / 4 times more expensive than a HDD. Your training time will be faster however since you will load nearly instantly your dataset from storage.

- M2.... hum I never used this. It's also more expansive than SSD, so I'm not very sure you need this at the moment. You can spend your money on better hardware instead.

For boot / Root of your linux system, using a ssd is not mandatory, again, linux is faster than windows, if you tweak it you can reduce boot time significantly (one of my teachers actually achieved to boot in less than 2 seconds).
Expect however longer boot time if you are not using a linux headless (linux server).

It is recommanded to use a separate drive for your os / boot and one or more for your data. Linux need 50 GB of storage if you put a lot of things. You can also go with 20 GB.

### Cooling the beast
There is three main kind of cooling available.

- Air: basically you put a big chunk of aluminum on your cpu / gpu, a fan, and yaay "conduction and convection" will append

- AIO (or All In One): this is water in a closed environment. It's more stylish, but not really better than air (actually some Noctua air radiator are better than AIO).

- Watercooling: here is a very stylish and useful way to cooldown your components: you put pipes with water in it. since water is a very good conductive, the heat will drop a lot. However, this kind of cooling require more time to set up, and maintenance at least once a year.

- (other): there is other kind of cooling (like Dielectric oil, or sub phase change where you cool the cpu to -50°C) but it's very complicated. to set up, and not worth it.

You can expect the following temperatures:
Air : CPU: ~50 °C / GPU: ~75 °C
Watercooling: CPU + GPU: ~30 °C

If you live in a hot place, watercooling / AIO can be better

### PSU
we're nearly at the end !
So now you need something to convert electricity from the wall to you component. 
There is multiple type of PSU (power supply unit) with 3 main things to look for:

- Efficiency (80+ Bronze, silver, gold): it will indicate the efficiency of the psu. So Bronze psu will draw more power than silver ones, etc. **DO NOT TAKE A PSU WITHOUT THE 80+ LOGO**: this is an indicator of a good manufacturing. PSU without this, especially in high computation are a fire hazard.
All brand are less or more equal (if you take a PSU with the 80+ logo)

- Modularity: it means you can unplug the useless cables (for example if you only have 2 hdd, you won't need the 4 cables)
Semi modular PSU mean there is only the CPU cable that can't be unplugged

- Wattage: This is the maximum amount of watt the psu will provide.
You can find various calculators online. Be careful though, manufacturers tend to increase the wattage needed to sell more expansive psu (so don't use the manufacturers tools)
[HERE is a good calculator]()

### LED
Care full some component are shipped with led everywere. You will pay more for the leds, and sometimes the hardware (especially for fans) is weaker than their concurrents without led.

Linux is not supported by default also by the manufacturers, sometimes there is drivers to control those leds, but it's not always the case...
So don't put too much leds in you build if you want to avoid the rainbow puke ^^

### Fan
Just make sure the fan is 3 or 4 pin.
If you want reliable fan, you can go to Noctua, they are designing datacenter fan, and their guarantee is very good

### Case
spend the rest of your budget on a case. Make sure it is well ventilated, or your computer will become noisy.

Make sure there is enough room to put your radiators, and the motherboard. Mind also the GPU lengh.

### periphericals
If you are using linux headless, you will need at least for installation a keyboard and a monitor.

if you plan to use linux with a desktop, you will also need a mouse

### OS
*Not windows*: some programs are not natively supported. Also the official supported OS on most libraries is linux

if you don't know which linux to take, this mean you have to go with ubuntu: it's an easy os for beginers in linux. It's also the official *most* supported distro.


## Youtubers to follow & useful links