## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:35783b21f785f5d7d602213c09ffc7b3ce97fa98b4ca9ace8f9f707cffccc631
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:d0b12954b511822d27b420407b7b8221765b004e7c34c2206d7bafd9c0767ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60317116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a4edcfff2b736184291de6ff4d9c8c7009e439576422315640f6d351cf4d25`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:26:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:42 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:26:42 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:26:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:26:45 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:501906f379a13fc3675791cbd6304f648074973affcb965be0bef8b0aaa34ab5`  
		Last Modified: Tue, 24 Feb 2026 18:43:03 GMT  
		Size: 48.7 MB (48677181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f07e04ee6c6d7e1e73fee33f43ae76c94665594b27fd8219d5901d1e2a13b5b1`  
		Last Modified: Tue, 24 Feb 2026 19:26:53 GMT  
		Size: 11.5 MB (11545761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:383f1068804ccdefda161b939dc5a3f3563a8df73ed8f3f3096c461a83abe196`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f8203c83c716a78aa15f11aafe864559538ce354425197b760da5e7abe08d0`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a72197a802ca72e0f16f7b8cafe6d26e8c8d6a943548bf53d35eaa8237d4c7`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 90.8 KB (90818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fbdb58a314fadcedcd3c7b6d481fb4ba4ebd9b8caae1f9a6c62c3ecbf53b3d`  
		Last Modified: Tue, 24 Feb 2026 19:26:53 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:bdd2fa846b292e7cbb79d361179e5c8880ad91a46e85c3e0893cbc1545351bb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3620387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f691c18746fe373387de85684aedce750b2a0579f20270c954e35b93fabd8f68`

```dockerfile
```

-	Layers:
	-	`sha256:c2a56bc4ce17dfe4edafb4c8a6e38b63921cf94dadd07d2a4158f062fcf11b4b`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 3.6 MB (3604429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc1e9db9f65c0e865f577724723b6a52d11fc50178268cb3a7b2a39070a5f184`  
		Last Modified: Tue, 24 Feb 2026 19:26:52 GMT  
		Size: 16.0 KB (15958 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:73f3322b7d1ae49fad3752fb5ddaba5846e2f2d0500ebee9b52fe3974ced20b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60059426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3312f5802e6f1c0960668dcb5e03dfd06fca42e3b1604d18226d10674501afe1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:31:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:31:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:31:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:31:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:dc3ce43fbcc581a6cb3e0909e03d7e31c0ff1d4d76469e15d6610d1403f2a7e0`  
		Last Modified: Tue, 24 Feb 2026 18:42:39 GMT  
		Size: 48.7 MB (48705026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a62862dbf8db09a903a15d353217d9a365042a8b798672096e82994959cde6`  
		Last Modified: Tue, 24 Feb 2026 19:31:51 GMT  
		Size: 11.3 MB (11259528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d5f6662a6fa16ef721d7e010df4406e5fede511c8bd0d79afcfe9965472af0`  
		Last Modified: Tue, 24 Feb 2026 19:31:50 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5587a0c6c01000d0dbde06b3d462dfb3adae85367b1fb9828c9306350877c7`  
		Last Modified: Tue, 24 Feb 2026 19:31:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee918c1f1b970b180d3a145e9d7800239a571a3ed6870f3a845404ad598b48b`  
		Last Modified: Tue, 24 Feb 2026 19:31:50 GMT  
		Size: 91.5 KB (91516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e114d64cefbd013e38d8464835714f54be353fba6212f0c5d78da4395672d5a`  
		Last Modified: Tue, 24 Feb 2026 19:31:51 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:48718b18274a096e85c9cd5211435ccd1f9817c57c871546e57452b4dc81aba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad152753c75d8279d2cef3ecc0617a67c04ab120476ca16c863b89a65c52f107`

```dockerfile
```

-	Layers:
	-	`sha256:19244e41f874e58521b8ab69169ebb5978d14b5dce4aada57554d8d2e23426a4`  
		Last Modified: Tue, 24 Feb 2026 19:31:50 GMT  
		Size: 3.6 MB (3613329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b9e4308a7764a883a6adbef81c64bfab35e0819841f9728799fd15c96e30faf`  
		Last Modified: Tue, 24 Feb 2026 19:31:50 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:d42438d38c9e079fd52dec3b87f71a69db6ad329810d30b4a74a15fd497dd63d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61898163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6cba92b75e83cb9da2baf094116ede347044c3828eb07fe360cc851e994e45`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1771804800'
# Tue, 24 Feb 2026 19:27:02 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:02 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 24 Feb 2026 19:27:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 24 Feb 2026 19:27:06 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:27:06 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:143f133830d056570eb26009a5886b146c40a6e16bbee60113f54a6baa1643eb`  
		Last Modified: Tue, 24 Feb 2026 18:42:19 GMT  
		Size: 50.0 MB (50011968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524fdb442bcdc44d4ae73bbcae7ab2f38f52fd1217e526a909240bb46ec3c876`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 11.8 MB (11791760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7777859d20e7915510216f2838b877ab508a630d9b9fa256cb8bfbac5e86fe1f`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 2.6 KB (2633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:839c0306b3e738a751937ef11586456a3353510e347a27690bfcb58bb043207e`  
		Last Modified: Tue, 24 Feb 2026 19:27:13 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e412fd9ea524b9d67b46800e09679b74ffa456859a1147f8e9875ca51b18fc54`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 91.1 KB (91083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041226683a6b62d22c988f073713102fda93eff7cb7f93695e37ae0e06e2e3d9`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7984bfd07739981c6b0780c475753fe299a8653dc588669e5b496e180d618003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3618302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054fcb9fae38125b183fe65bedce28f1e5e723c53468f9ba3f8ad56835c77ee5`

```dockerfile
```

-	Layers:
	-	`sha256:02a8908f86977b9b28bfedf1adecef170cbf3f7187762a3caa98472ed1f4a7b1`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 3.6 MB (3602373 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6240738ac0bc19fa3eafed4f8b150bd6ec0fc5e84aa9ccba13e058fbe037d74`  
		Last Modified: Tue, 24 Feb 2026 19:27:14 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
