## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:47bd31860c77adf496729c702ddf0f9cef183b1c7b7135ff1ff76c65952a33a4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:1425bd9e1aee2d8b829fe6f60c573976565e2db157ca795344af02a3318858b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.2 MB (59170368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eabc5957637bf252746d4ee8fa3c9557c75872388cd662cc34a9041fe9c22949`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:0ee0708ec9247cb19ad61d1bba3a89642d7eb4cfcd5031f23018c732b0ce201c`  
		Last Modified: Tue, 13 Aug 2024 00:25:12 GMT  
		Size: 52.8 MB (52836188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb951e649daac819b595ac587aaf218374e8b4c3bc3087ba695fac7b934eba45`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 6.2 MB (6241054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f038e90372847809ce4787019ffe2552665f1ee24e025408dae3af64a31ad5`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accfc3f0a6a00032ea0f0a0c663842971044c6aeac311d4125f722aa71a0389e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c314720cc1a281762827362053b361757ef353ecbf43d5087e73180343ea5ad`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 90.8 KB (90751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d58994bee8abc92b11ab4b444c3e25ac488693c2c7cb41084f5033169065270`  
		Last Modified: Tue, 13 Aug 2024 01:12:01 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ea1b48dadf464be5d8f7b5e22aa16d72f2f0dd37386de3115a688a21eb0b5d84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3547863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd84b85cd11787fa38071e74cfc3c3bbaea4fb3b57cc4206f89bd741a77477c7`

```dockerfile
```

-	Layers:
	-	`sha256:18ec6a52cd24db235d9d5944f71ac133a2d011cc2b0ec5b78c4ab1476b15c740`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 3.5 MB (3532434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e52e2080267d702efdcfb23a039482f22c00ce72808e220895ca7f265026ed8e`  
		Last Modified: Tue, 13 Aug 2024 01:12:00 GMT  
		Size: 15.4 KB (15429 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:bf133873c23d03980c9d3b650b754fd4f358e3e0e352eb32c15ff2f0f71a4c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.4 MB (59372858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b36d5dd60acbe2494379448b88f3860f372c0fb76e1fd36bfb41f506c36333`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
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
	-	`sha256:02deda8175a76811cbe2e5cd721980efdbc7a9d4ad836f3a0f7d07ac36ce51a2`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:16c1f738d55249a635030e91f4ea08ba5bf2b58aac18867449d4056178dae3bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3577265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e658cbf98e35d798d073a33235d32b9ea30ccd99ff3aa192c0c0e51ce3555df9`

```dockerfile
```

-	Layers:
	-	`sha256:04b19be0c9e27b3babc5ab6687d6d64e862a4b989d3feb1d0d1f1aa812493051`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 3.6 MB (3561562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f305496ab906cad0f4da0b7b7b5a7c6e3a2f1140d9dbd2afd4fed76ff1a231e`  
		Last Modified: Tue, 23 Jul 2024 18:38:00 GMT  
		Size: 15.7 KB (15703 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:3879645d8248e19c7cecc51e81e443dd2244460b4f358cfeb57cb286852c04a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60397770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffb0d7cc60a97195c40904e7573f816efef7d6f12cc2155af4cfb3e20b788da`
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
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:47aa20e0d3978e830fbdc52fb1b018e2dc37ff9f122461c55040f23300208844`  
		Last Modified: Tue, 13 Aug 2024 00:44:14 GMT  
		Size: 53.7 MB (53738474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b71d132a4344bb16e2e09fd83117250f48d572c643b3a712f89502bd494932f`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 6.6 MB (6566180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b92d44337ab2e36cf50dbb0e5f5a982aedb8ea031edfd566ea77794b8600db`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83d54a7d8728387f810ef105293ffd3ecdbe46c909d35465dd6ac692a203a66`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02c86223c48237f67a081fdc1da5b575bca1e0b24ca39b18348f604b229ec46a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 90.7 KB (90739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c730d96f05d4551706957182b16dc3e0b695f848bc18e53ac8a87794f7bc71b5`  
		Last Modified: Tue, 13 Aug 2024 01:12:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:afa48e552f3090b92141c3f16761ea91ebd9c37674b87f9131690f18413b23a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3545741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bc69503183698682084ccc15450c076f8942d02054a333aa86200e39f668a11`

```dockerfile
```

-	Layers:
	-	`sha256:d17136678b054f4bbd69c0d37627fc779e2d83be22dc0d59ec71ef570984beac`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 3.5 MB (3530339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1d4f4372fabf850ce1ffa73ac663ea1660175de7920a8b704f09006156321a`  
		Last Modified: Tue, 13 Aug 2024 01:12:02 GMT  
		Size: 15.4 KB (15402 bytes)  
		MIME: application/vnd.in-toto+json
