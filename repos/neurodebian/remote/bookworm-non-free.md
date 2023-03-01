## `neurodebian:bookworm-non-free`

```console
$ docker pull neurodebian@sha256:e5376ee5c2816d1efd79bb3eb467663c377df44a2eabb9430ef9b0e9474231fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:bookworm-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:c248a7d665bda19d273222a908fa5850c1f1380317d8bc4916ae925e356167d0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.0 MB (60987511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d056149a345cb8309ad04642bf342a4b3f0c1daab681ef1b62aadf6c4c6806`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 03:19:36 GMT
ADD file:99a61197d7273704581c44eae01f3342e9f3562e84fe66cc2d56ce563e58450a in / 
# Thu, 09 Feb 2023 03:19:37 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 10:33:25 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:33:27 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 10:33:27 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 10:33:31 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 10:33:34 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:45c04dd46fbf614b423b54561d34c6339a0376d1717729ef6dcf101dbfd20f8c`  
		Last Modified: Thu, 09 Feb 2023 03:24:14 GMT  
		Size: 49.1 MB (49054961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38236192934019393b60f6a155f92e7625f86d7040a25abc85f16331e3f20a9`  
		Last Modified: Thu, 09 Feb 2023 10:35:12 GMT  
		Size: 11.6 MB (11649251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ce3c24436d316066f2f512361cceecec6597a642758cd8a30a7e6be8045177`  
		Last Modified: Thu, 09 Feb 2023 10:35:11 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c3b6867a3b8b7a0990aed29d11f0ca7d3451728e8394e1ffd435a9860c08c`  
		Last Modified: Thu, 09 Feb 2023 10:35:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3878ef31203d1f458f083c3adf2cefb760dd8bbc98002c0732519fe24393de`  
		Last Modified: Thu, 09 Feb 2023 10:35:11 GMT  
		Size: 280.9 KB (280853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec51a2c8898f4455cebcb45cced98d389e9c9f0dfd468a9540f6529c412742a8`  
		Last Modified: Thu, 09 Feb 2023 10:35:20 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:e7370003f0ed9dec23acc7f29b0815ab397afd432b2df18e599b9b102e89775e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61219181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7c0832f70f46788003d977bea0b614e36cf4bfcc2cc3adc779aa0e040d55ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:13 GMT
ADD file:5b81699b80066f9e3bc967bdf130a67f54ebe15cd80df6c952262d6132b1cabf in / 
# Wed, 01 Mar 2023 02:20:14 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 05:00:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:00:57 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 01 Mar 2023 05:00:57 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 01 Mar 2023 05:01:01 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:01:05 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:cf639a903cc04a00c81ac77b3b9f9a79644c51b7f515895fd60403c20ff34a80`  
		Last Modified: Wed, 01 Mar 2023 02:23:22 GMT  
		Size: 49.3 MB (49273990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e7d14f29f2eb167ac51f770477e6bb0dc04420d33cf62f394b42808e7a2be5`  
		Last Modified: Wed, 01 Mar 2023 05:02:43 GMT  
		Size: 11.7 MB (11660961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a09d88f16d7c91eee89e9b9d217651ece28e60d5d05f92faa251979afebb8b4`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2a0f8f7c18fdea22fd3298506359948881eaa1e6c6c7190649cdcfbbe622fb`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcfd5333ecc9ccbfbcabc553008048704eda10d202384c917d7dbd5d1a84cbac`  
		Last Modified: Wed, 01 Mar 2023 05:02:42 GMT  
		Size: 281.8 KB (281784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bfbe0c4ee6dacde7a5bf899793444841c5a20f08af294bad3a3a88be2ef2be9`  
		Last Modified: Wed, 01 Mar 2023 05:02:51 GMT  
		Size: 432.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:bookworm-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:e493c2750ddd7876325a9c6ea61e4151508765499ed3754db677899a97357fa4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62066068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5dcb21fdd302fa0b7ef1f3c0c90c46056a0b4f1f86854e59113ff43965f7a7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 09 Feb 2023 05:12:11 GMT
ADD file:37cc85485a8f79a4bd5557a42685805da0b367ff061d53fdf29d5f242593ea1d in / 
# Thu, 09 Feb 2023 05:12:12 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:43:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:43:52 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Thu, 09 Feb 2023 12:43:53 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Thu, 09 Feb 2023 12:43:58 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:44:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:0153a17486e7cd96c30b54f1d68ab1cffaca99de43335324f16477807b1ddb1c`  
		Last Modified: Thu, 09 Feb 2023 05:17:35 GMT  
		Size: 50.1 MB (50089500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6187a90aef6870d09282470d3b592e152d72bc909d4c41fc4d2a0dc6e35d578b`  
		Last Modified: Thu, 09 Feb 2023 12:46:01 GMT  
		Size: 11.9 MB (11882490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4ad0b3bec733e0fea46c5f1aa52aba6533737fae1c7ed922601bea2dbc7dbd`  
		Last Modified: Thu, 09 Feb 2023 12:45:58 GMT  
		Size: 1.7 KB (1742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52056b4dd31d6fd76427109e57655ab7cdb36d3cdf6287f75d9ba2f4c8dcd0f`  
		Last Modified: Thu, 09 Feb 2023 12:45:59 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8502cd76b08bed33327032c663ce30112feb1286d449672cffdf1346457ab1`  
		Last Modified: Thu, 09 Feb 2023 12:45:59 GMT  
		Size: 91.7 KB (91655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57ec70962ca1ca64d913ade6eec99635035751b50e604d663e868b999958779a`  
		Last Modified: Thu, 09 Feb 2023 12:46:09 GMT  
		Size: 434.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
