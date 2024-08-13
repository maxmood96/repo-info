## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:ec21c66ad11991c909e5156c608f29f244cfdb83d126b82669806fc90de88175
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd` - linux; amd64

```console
$ docker pull neurodebian@sha256:0c49e4a33023f609f09584e01a96d87c68a121e96515944c5f3742046a1131d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59170126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebcbf25b3d7e2dedf834db3c4f16a5666b581e8ef4a7b61bd7a2221053e84b07`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:ec9b256ad5af9d6c88b912d94fd4e58256e2b29a1c5ff616fe47488c72c1256c in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc89778f0cbe977174713de355013559ccca9aa08d5b5b559e431b5bd430fab4`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 6.2 MB (6241198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91e887a135a43718b8a55438286ebe39af3c8d90d51c7777702b9975eec68eb7`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f923e5ac6535fb231a908057bf7bf9c5a189cb99940d6b80b697a9197646b238`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a858564bc043dfb29427bf2f3af58c4ccb39bf59727d42f4b231d5d1c591ce9e`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 90.8 KB (90755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ef82d2130935bb1c751f0ee18ba8240b2d6756d043b12ef03a7f10017b9d1d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b60949604cf8301350f811495e1b4a1c190193e428919143b5699ae94506c2ea`

```dockerfile
```

-	Layers:
	-	`sha256:c07e1a9590f3ec7c50f2087ca0e87be26394b0ea852bf7b6e99d665e12b9ef7f`  
		Last Modified: Tue, 13 Aug 2024 01:12:06 GMT  
		Size: 3.5 MB (3532398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:862a30da3b7805baa8efb3dd60a274fbaf4f01dc944ec7841862bcea4cad736a`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 13.4 KB (13397 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:8c95c9493701e6ce942dc6bd4246781a631d9b5197e631b6ae293949023ccd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59372464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82695e6cfe4adc6f346d5c84bbf1bc7154bcd6669f2a0d083c38ea98d34cdd67`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:368e6d1d2999bc62054217cfec29bdcf59fe672d1d5db07c2f2c2939222c4a42 in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:88161cad314c45536b001a7558a18c0a54c991650605a6212e9720f7ac3bbc4a`  
		Last Modified: Tue, 23 Jul 2024 04:21:45 GMT  
		Size: 53.1 MB (53060158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5e22eab6bfb0637511700afc2f7acd0c3fce57b42bad64a4534c5c34f2b23`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 6.2 MB (6219604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88300873cb59f94a9b5b736e89bc5fdec8a6c027a5aa343e28fe5596a82a1177`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9261c28300bccbc9dc3a8f5e25c8ec61266871386ae0bf74f7f95402d20b353a`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a368fbf666afd365681e06a696c68bc93362d632f6326c8caead3c876de84885`  
		Last Modified: Tue, 23 Jul 2024 18:37:43 GMT  
		Size: 90.7 KB (90721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:af51a66c271250ae8a200c0aacf5743141c34b74875ed711b01d39de1fd3d171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3575196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d942133d8a2c4c5122c1362446eb9237ac2b26dcd3dbc033c75e5120c0ff5049`

```dockerfile
```

-	Layers:
	-	`sha256:dad4a51b19f92441f221131eabd713c323dd07f9199d2cc5407851b23d413a20`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 3.6 MB (3561526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2161ab33b33d74b6035e8bc891ad6b32b14e53933ea34e9b1c0c298e9b95d0fb`  
		Last Modified: Tue, 23 Jul 2024 18:37:42 GMT  
		Size: 13.7 KB (13670 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

```console
$ docker pull neurodebian@sha256:2d7295e78c1f93e93a2fafe3cf5d6578c9bd04ba3e70aeb1ac00e4ab6a423853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98da68791e8c85b2337b5ace3354f2cf5c2661f1890b36c48faa684596d1a893`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
ADD file:79c443f9d7d3c4ead1afa700b0409049a5e5def4db762097116c9f15a44a29ca in / 
# Fri, 21 Jun 2024 21:57:43 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0659bfc4fa78a1d35cc72364a5ae98ac8f4d07bd69d5519d26f5a17cb400a074`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 6.6 MB (6566071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8727d0f61d96321e8ca009fce720e24d7cc8b2eef994ca6bc4de03fca1eec706`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d6a36b20258ae61eb5dcc9eb1db3b6f8b4cc8dd1758e38b36d1ba0854ca92f`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08afb7bac914d3affff0a203687d081a71dfea865fb144968f617538c675d23`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 90.7 KB (90690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a550bba3856e784dc5634debe1d9eaa3713a572c52b7a21ec54d73e0c2cf13b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3543675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab79690e1cadf319dd8b38d9a493570fc9e9c614dacf0dae87dbb78b2feacbdf`

```dockerfile
```

-	Layers:
	-	`sha256:1a0d28cdbf8efae3239dea7c48eb32f819b4f35eaba78d926a86bda35ae7add8`  
		Last Modified: Tue, 13 Aug 2024 01:11:56 GMT  
		Size: 3.5 MB (3530303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2c286a639d57592fa8d3072963de485396b9c4aab261687c908e99b643ae588`  
		Last Modified: Tue, 13 Aug 2024 01:11:55 GMT  
		Size: 13.4 KB (13372 bytes)  
		MIME: application/vnd.in-toto+json
