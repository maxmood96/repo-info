## `neurodebian:forky`

```console
$ docker pull neurodebian@sha256:f5c1400b64154489238008e08525e740f68fdcb64fe5b531cbd990ea69a7627e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:forky` - linux; amd64

```console
$ docker pull neurodebian@sha256:345b73cc3cff330f591113ad5c395e6f1d6d41737f1aa30d2cd0890eec290e20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29205c954925c1ecb55bac9ed0b80d21438ff3c4f7a6310eb2538739681d65a7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae5466bb071b4d5fd8eefcee42963b6fb9049be541a84881dc6308e473fc8e`  
		Last Modified: Tue, 30 Sep 2025 00:16:29 GMT  
		Size: 10.4 MB (10379739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1807ebbab503ae80b9399051b61f04755ca3d6aae60f4dc6d425a0bf7720c092`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd66df67e8d400f04c58dbc6b030e39a1acf8a05e6146909b24aa7170753dc9`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afa15f7f278e086ea0fbfd80f89d1c5006e7335cfc7be13c9460227d1cf6fbef`  
		Last Modified: Tue, 30 Sep 2025 00:16:28 GMT  
		Size: 89.8 KB (89801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:852b8be1f7037fff7d287538ad33f1cfc8866e29620587784f5b9d583b107b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c24d1eb59953bf3dbf18bc9e6d60ee7930713fcdc584cf97746191124cd2ffe`

```dockerfile
```

-	Layers:
	-	`sha256:85f5c52cfdcf421d688db7359c6af95dcbf0fdc4dae316f1ddff761a459c067c`  
		Last Modified: Tue, 30 Sep 2025 22:07:43 GMT  
		Size: 3.6 MB (3603543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e92428ab852a3e9d6c4f35263068e7e9d1f55e02615a19121b450e71837a5a`  
		Last Modified: Tue, 30 Sep 2025 22:07:44 GMT  
		Size: 14.0 KB (13975 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:1884f414d7f4d42d9194552cca4f2f561cb5c831930c25069ca8dc52b51d7600
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed2bf448f9d640a57c8d25e475b948218b398464dae0079c10f902a6bc5e682b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Sep 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1757289600'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b389e1eb5e3644c29fe20800e97ad88d4130d8f91f2afd0935089cb492e67d`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 10.1 MB (10143305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdcde2bbb2b8e25a5f487a9ec062838dbb061b545dc78378db54ab4fe327e022`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 2.6 KB (2638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedaf43c0ade1074e3f4761d8a0db8d3cc800c99518e23a233f454ba8272e3e8`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:322389dfacf69a954619302405610c10bf093a760bc966f8abaa9a575fc47919`  
		Last Modified: Tue, 23 Sep 2025 17:39:30 GMT  
		Size: 90.5 KB (90538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4ae4111f9fb4f8661c3112d2c2094f3af49e04a1628e6b9d5807514493edf440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3625269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183abe123d0c6b4848582b78924a88e96c0a8b2551abc83c0ed2a029c8677f86`

```dockerfile
```

-	Layers:
	-	`sha256:1c0cab0102cdf0749d41ec86eacf9634fdd3b97d0ef197c01d483a01c4ccc770`  
		Last Modified: Tue, 23 Sep 2025 19:07:24 GMT  
		Size: 3.6 MB (3611171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d1aa1f7c47c6525788e4cb300f8b8deda3a356c92a5e3b51068340adbbbd84a`  
		Last Modified: Tue, 23 Sep 2025 19:07:25 GMT  
		Size: 14.1 KB (14098 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky` - linux; 386

```console
$ docker pull neurodebian@sha256:93076c4c2d0e94886018f69e1152e8deaf2d4bed3e6efbcbafb955ac2a8821cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61744597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c512496e92c8a2ab4d459299062ede4abcb70e38f111d2e6aa0b505fac923153`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Sep 2025 14:32:09 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1759104000'
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 23 Sep 2025 14:32:09 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a865d211977b3f1fcb807a758d4ec086437dd6673f67e3e1d591e17e58882cb0`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 10.5 MB (10532079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91719f443526b031661e5a96a385443574e851a066f71ada0666f70884b0e2dc`  
		Last Modified: Tue, 30 Sep 2025 00:23:13 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b17552004c93b6782e1e3a7a419888801d004eedb43de407b78b4ea866fea1b`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 271.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d093529586e174c24eba4daef5bc737d33409e0ab114788aeeaecda34415aa42`  
		Last Modified: Tue, 30 Sep 2025 00:23:14 GMT  
		Size: 90.2 KB (90191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky` - unknown; unknown

```console
$ docker pull neurodebian@sha256:88c49151d58c1387ab21df41ef3530d5a8bac401ff1fe37dee65a3caaded9855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3615449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdd154be2b8b9d7924f741cf7a9dddc57d872f8fb9afe3536f35a8960c6cafa`

```dockerfile
```

-	Layers:
	-	`sha256:154737cd4e2fe16fcfe2381c2c77298084a954fbc4a92d2a4987a4f405a1af1b`  
		Last Modified: Tue, 30 Sep 2025 16:07:47 GMT  
		Size: 3.6 MB (3601504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6407fcef5a1ef280b76d26fac524a4f6552d3ed6baa7676692a8c113201710a`  
		Last Modified: Tue, 30 Sep 2025 16:07:48 GMT  
		Size: 13.9 KB (13945 bytes)  
		MIME: application/vnd.in-toto+json
