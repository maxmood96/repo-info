## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:ffef758c80ceabbba337660d9965eb402f9211965a7659511c9648332d2c09a1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:trixie` - linux; amd64

```console
$ docker pull neurodebian@sha256:da3b9227f84c0e82c2a1cd4cb5e96ec28789730085a1ac4652b6bb91620d43a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59678819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be8b026c74f7c723c4dd8ef3d34903dbf19b1ec0bcfb0356313abfeee3f0d4a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1769990400'
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:48:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:48:56 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:48:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:ef235bf1a09a237b896b69935c8c8d917c9c6a78b538724911414afc0a96763c`  
		Last Modified: Tue, 03 Feb 2026 01:16:00 GMT  
		Size: 49.3 MB (49292952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae41ec031155c98b455bb78067eba48a17546176cae679a09109c6f40044b853`  
		Last Modified: Tue, 03 Feb 2026 02:49:08 GMT  
		Size: 10.3 MB (10292604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08c456de52ce89d78c3e11be3ed11cac3ff2a3bbf1b5b7acbcc34864caa6ed1b`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901c3f547274c1b9aba5a4c1dca0de6439e3641e2927b7ff0e29ba10f2598771`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e44b0ddaace5231fb0277c41a8f1dd1b9a803222537517cf5fc0faf0163b35`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 90.4 KB (90356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:0af8d1c9f950620612b890e7e6a4d8c5e0b2b9f2e5fdfb0bced7707c0f81c1aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a741a8c1833792cc9553aecb085450cdb9f1664685ce094c1941eda5289f656`

```dockerfile
```

-	Layers:
	-	`sha256:e40985eb60787ad8aa5df064ec78906a87d592650d3cb7bd4e4d35fef41aeff0`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 3.6 MB (3614068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c276c637f8dbb8e68f06bb64f124d7e82ae5dde2c17bdf3085ab2d27b05e7a9`  
		Last Modified: Tue, 03 Feb 2026 02:49:07 GMT  
		Size: 14.3 KB (14251 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:07e1a111cf7db99a4e8da7b30d05dbe05ce582c3e60c621b8dddf3f1d7fb85e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59815799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6958c992473c935b57387a0074e6ff9d5c8d8f25f4000cddbad2a4da7337e949`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:35:37 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:35:38 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:35:42 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:5582010cab7f00a8f96e076b02666116eaa7e4af9a74eb44f2946a593b50294f`  
		Last Modified: Tue, 13 Jan 2026 00:42:42 GMT  
		Size: 49.6 MB (49648083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7684c225310a7186686d90420bff2204e00d1da54ed64629dd5c3e06bedb11`  
		Last Modified: Tue, 13 Jan 2026 02:35:51 GMT  
		Size: 10.1 MB (10073782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f6a425fa7aac586d22520ac0e48d6b900e2d7650c99f069fc369de3faad44f9`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b744125fe7f349b2dca35775678901252ef655baabbabf00e0581e5db35f4d0`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da1ec7811cc5fffb4d35b28f25ffe926c9d946a0287fc98559205e5ee8aad5d7`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 91.0 KB (91029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4f8ea8e151623c0726e2b1d500eadf97f81d9185d53345068d8a5310be376250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3629982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a8d3f945473a1378792d3153caab159049530a28c11f85defc0c8257070900d`

```dockerfile
```

-	Layers:
	-	`sha256:9036dfeefff31d7ac9375bcbcaa30955c898c61f27f40e393540a89d7cae685f`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 3.6 MB (3615595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e69148b190dc58c8fbc910cf582b627d0d34da0969ae22d538922ec69e3487bd`  
		Last Modified: Tue, 13 Jan 2026 02:35:50 GMT  
		Size: 14.4 KB (14387 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:1c485a7ec0ef76060f194fc63ade360521156d06352d21ba7e55c5678263b4e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61359266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3405de0f825036ef97723d3ffeaf81ee462ad3c0bdef73f83566138b62c01017`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:11:21 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:11:25 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:1f0b243ad587d8f60f107748ba9fe54e338921c7b90e6a5d26e1d50d32f7481b`  
		Last Modified: Tue, 13 Jan 2026 00:43:28 GMT  
		Size: 50.8 MB (50798876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848f9978ca299f165c197622edd759b69b3cf32899ccbb3854492744e5131a0d`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 10.5 MB (10466724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcdffb0278580783eda7f81d2d70ad20bf0b440ee7b7590e521dc0aa44d3eff2`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d29a632dda1a11016736a63fec3296211533322f93651cd5c2f440ed3ea8f04`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f369e3c2508700e6055a1900113ae937b42ec7d8683d5ef29fc8b48f14b44a`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 90.8 KB (90766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:f1147e07d7974976c8157d340cbacd2696887d306fdb7a9521442243eee0bd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b93d8778ceb78ab3c09d834438ad8647adc746cb80d84fc2b182f923c0d074b0`

```dockerfile
```

-	Layers:
	-	`sha256:a32e0b1b72a70a565da4eddb3e9eee98754724c4b9777ad9defe87db52ffbf4e`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 3.6 MB (3612016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acd6ffeb7dffa3512f65e180c61eb1ffa3c36f0545d4818f3ec30607974a2b26`  
		Last Modified: Tue, 13 Jan 2026 02:11:32 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
