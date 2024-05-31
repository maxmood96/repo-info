## `neurodebian:bookworm`

```console
$ docker pull neurodebian@sha256:9773bbfd3b4cccd3631acd50338ded5d75b2f216346165e62ce31122c0b93dfc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bookworm` - linux; amd64

```console
$ docker pull neurodebian@sha256:8003ddd6f73b7806bc9583ea35d61132dc3378a3b194e0194fad7d3611cb95d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60937750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fab80b10beb2a161f42eceb87ee4ba0552673f0c26475cd6eb2f527b436ec3da`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b9a9fc37b874060c713002ae1ac220f097edd7c6576116c22bb15aad8229b1b3 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:c6cf28de8a067787ee0d08f8b01d7f1566a508b56f6e549687b41dfd375f12c7`  
		Last Modified: Tue, 14 May 2024 01:32:07 GMT  
		Size: 49.6 MB (49576390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d0d5ec172ba144071ed0223437f3e4b990d14a4ac73b3f8aa119fdec79b9d2`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 11.3 MB (11266570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31940436a11ab29fc862e2d14d020075964dcb59f967bff291d857751bd4d197`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6de3ad8d62b9a7799615ee74064490747e19dfcf3c526742a4e60bac1397b6`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9baa1fb88a8638cd71a6802afce4c4b8e3980ba78a41930dab72ae419205b7`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 92.8 KB (92801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0aef42c6e0933296b5b46229b5757715801e8e0cbfc579d6bb261a5900300dc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f8dc494e821e0ec0217ed94cb1b13b95699d0d150843aea5001b45df309e4d`

```dockerfile
```

-	Layers:
	-	`sha256:257120a633cceccddc68b5f94e49b59497b162ca95753b43f3396da277ab65f8`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 3.9 MB (3901743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c08d4dbe78cc309275b9c9eec0dfc9bd127c7b5d47601255c335c2ae6b2757a2`  
		Last Modified: Fri, 31 May 2024 00:56:57 GMT  
		Size: 13.4 KB (13428 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:6213e2c292c45b49cca98fe498a6808f2700584a9628e3a5624664d9840b87ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60940537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6100f105e85e080929e093c60771b4ca4ea252a385959b9b340af469a157696b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:b7c55dda8ded4219a7cdc9fbd91dfb5996c4886d4394b85751c2f956defe3287 in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:91e301773f03e9e0fabc5c177fe6bfe8daf14e992ab816f151692b814ddc462c`  
		Last Modified: Tue, 14 May 2024 00:42:35 GMT  
		Size: 49.6 MB (49613388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9782ebad61654b7a2473c30e527f7a02ef0ff05bbeecddfa2c2a63f5e2e99048`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 11.2 MB (11232082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81ee0a093ea753330fd619da92cd9d8620723145c8a836f8b74d64edf92a5d14`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05e17f23f6fb69d4dea07617d31ead77946fcac635bc98263d0e0edfd62d3a4`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b77a1d67cd06ab552ba0ded4026133eecdee96d5c48543f468b3922517a9c4e`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 93.1 KB (93077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:54701503357d38dbf5ace89b77543c8fee2f2b62adb377e7e960062c2516a02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3915692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd05fd8622dccb239d931c85ba833255c0c1529b61cee5e678e8a219b7b04f8`

```dockerfile
```

-	Layers:
	-	`sha256:faadff5adb164e444a55b837fc6ce43c32d2f30627d4d1a82359fb8fe02245f4`  
		Last Modified: Fri, 31 May 2024 14:44:20 GMT  
		Size: 3.9 MB (3901984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01cc38b6d237c2ebcca5ba6cf809711edf85703898a921cc5c6525ad6628ec43`  
		Last Modified: Fri, 31 May 2024 14:44:19 GMT  
		Size: 13.7 KB (13708 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bookworm` - linux; 386

```console
$ docker pull neurodebian@sha256:f883c8d3cd6e12f48fc619289283baf20b1c608accd0a7c4b7b8131a714b7408
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62386288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070fe0610f01bda6386a382aad643fb97709abcd61c948b52e8e2470d255b724`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Feb 2023 17:48:33 GMT
ADD file:35709674a3b845511a896af16ea37a6022e7d48992d3198d0760c0c3208fe4ed in / 
# Thu, 02 Feb 2023 17:48:33 GMT
CMD ["bash"]
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Thu, 02 Feb 2023 17:48:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:4f2f2f6205661e555e772749ae7fd294fb04fc0d06cbc67a50a11fbb4ef44242`  
		Last Modified: Tue, 14 May 2024 00:51:31 GMT  
		Size: 50.6 MB (50602424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87883e412d578267ebfa0256300851e70ac03359e34eb6a8806a0b6b2bfe9b4`  
		Last Modified: Fri, 31 May 2024 00:57:00 GMT  
		Size: 11.7 MB (11688974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47283d1ad6416b00593137847e9022ec659e9122a62fe5351f240b63fa76ce48`  
		Last Modified: Fri, 31 May 2024 00:57:00 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ed3764b3fcfd4f5a2510f6f18acdd88a821e7b9278bb0cfd56cc715235a8186`  
		Last Modified: Fri, 31 May 2024 00:57:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2d6fca37744ae01a200c30d779c0549bc2969e493b43547d9360966532d9db`  
		Last Modified: Fri, 31 May 2024 00:57:00 GMT  
		Size: 92.9 KB (92900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bookworm` - unknown; unknown

```console
$ docker pull neurodebian@sha256:59d048893ec6f2723474fbae26d7e6985b43132e614f935d2159b2562ce93c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3913067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6768869e69eaf7aba70becc126b3296c3208de12cfbdd92965e5b8f7b2be0ee`

```dockerfile
```

-	Layers:
	-	`sha256:c2b6fdb5562ec89b3761225df0e24410f058ff848c59cfb475f4528a970a2ca0`  
		Last Modified: Fri, 31 May 2024 00:57:00 GMT  
		Size: 3.9 MB (3899664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ea339f4bdbb38f1374cd0381f8a0f2de4ef17c8f3cfa2a49ce6414a55157f21`  
		Last Modified: Fri, 31 May 2024 00:57:00 GMT  
		Size: 13.4 KB (13403 bytes)  
		MIME: application/vnd.in-toto+json
