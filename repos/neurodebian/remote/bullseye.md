## `neurodebian:bullseye`

```console
$ docker pull neurodebian@sha256:0b737232c9794e792613e2948c2dc646da73742794d05989706bdda85dadfb98
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:bullseye` - linux; amd64

```console
$ docker pull neurodebian@sha256:948a806d10e8de99412f13e48921d95a685331e685fcc5407941162c24a64d96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64970379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c739e12ee1b66df8b53d57247ccb7d3ccde3a9da7ade4e337147027212c8c8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb0713476e6838e62fce3e969ddf9e132bfcb3d7e2381b96a3e6590bea17355`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 11.1 MB (11103472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8c97eadffb1f79f36461db289f9d13b34abe3b10d6b2212fb7cb568f87c88c`  
		Last Modified: Fri, 08 May 2026 19:44:17 GMT  
		Size: 1.9 KB (1894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bb74a3e1d476d5675ca0b0ec9c21c09ed0ceb2776c8b0b4d9f6211687d86722`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19972676d50f6a3f1df56d9a06783980125881e306a22240dffb30771d4c04d9`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 101.4 KB (101405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:ec6f6d915f962e6180edb45f9e2b0ed07d34d1a406ca966444a00063bf5c0bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e318efab8b68b3a161ff0ded8b0cbbb53f5f184fd83aa7308634335aff71761a`

```dockerfile
```

-	Layers:
	-	`sha256:2e54cd4f6b03da76b043ede7315e1c5f2c6bee9f880f71566cac57f4127ab4b8`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 4.4 MB (4367914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:848dd6c010f74e7c1081c9108123e2b50de591b2f2cc38e0e7e07b7bde117f73`  
		Last Modified: Fri, 08 May 2026 19:44:18 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:62347cb324bd70e5569c022cf36e136aa8e826f40f1c2238889b719f8cc66a80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63466561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:088aaba085173fd83cbf817a16c6e4af04bdc9ae9eedb10afd7c44e3489ddef4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:45:49 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:45:50 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:45:52 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49da93cc2679b1db042cd202e875060e5e3220e87732350bd5904898892e8b8`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 11.1 MB (11109914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b825eee855070f51dfefec4cf70685dd607f1dc1402855869b4bbcaf7b576135`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 1.9 KB (1893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3209c067378d18d75a18203938000ce323b7b747348cca016301c372c516e6a7`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0c848bef723aca7f046b18ce448a4097239a1da120f540e52dd1c9a68a4b31`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 101.3 KB (101279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4243308f1b786a75f6a0506780d5c7b33ac30f8511fccca56aec4dea210c21b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4381612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e762402feeb4d06253b996167883d80d3641bf9e0680cf01273d11c016d6d5`

```dockerfile
```

-	Layers:
	-	`sha256:b14f0dcc1c2ef0142185e8793a6e22f9422570c4ba9d2b6abb2cb7125ce110f1`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 4.4 MB (4367521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f2aa08681f076f24ce71cb639cc4949a46b91a1a127541e91c515a501664465`  
		Last Modified: Fri, 08 May 2026 19:46:00 GMT  
		Size: 14.1 KB (14091 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:bullseye` - linux; 386

```console
$ docker pull neurodebian@sha256:8008767bb706f4c4cb709ab5f06a757d417059201885cf55e86abcb4cb6dcef0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66311198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2c192eae3260d4134a76b7bfbe15ddfec137154687d3fa42db1128cb0fe0a4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1777939200'
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Fri, 08 May 2026 19:44:22 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian bullseye main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel bullseye main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 08 May 2026 19:44:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:caf67df8e858ea1242ba8175484d5f733d658c733fcfe8f173a3140308e3ffa5`  
		Last Modified: Fri, 08 May 2026 18:30:59 GMT  
		Size: 54.7 MB (54705343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e381fa04b31e7bcb9cbbc40e4bf2902f0c275db7edc7b0462ee8936db48315`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 11.5 MB (11502397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ab2eed64c3b37a86ab0b509b8f661cecbf7b66e171eaec9e5c546fa3036762`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 1.9 KB (1892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:134a997cd26a4c569d5d64a9da26466d3c5c487619a3e32f1c97969f13fa616a`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 265.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3596ad0c31ef351fa9a9305382ce6d40415c6c0b91c7298614f295de6c8582`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 101.3 KB (101301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:bullseye` - unknown; unknown

```console
$ docker pull neurodebian@sha256:42f660d3785330ad3907a27b2a3014a5478c77cb6a2ae7174a586851e2a97d2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4378370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f329d1467811d726f323694ba1065308a4220276c10e46100ba962ecb9c53f90`

```dockerfile
```

-	Layers:
	-	`sha256:a6c78a26c8ba94bd4d662a5f8aa1daccf0739185d688ddd88ead6c3050508785`  
		Last Modified: Fri, 08 May 2026 19:44:33 GMT  
		Size: 4.4 MB (4364433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad96a7377786062bdd01bea8d0bb1ed027db71956b280c297a74b774fa1ab0db`  
		Last Modified: Fri, 08 May 2026 19:44:32 GMT  
		Size: 13.9 KB (13937 bytes)  
		MIME: application/vnd.in-toto+json
