## `neurodebian:forky-non-free`

```console
$ docker pull neurodebian@sha256:fb8e7cbc672f36bc7961013c650d260bbc5bc12eece4a75f700d2a4b2c4f4392
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
$ docker pull neurodebian@sha256:f5fe87c1e1ad0cc109f0cf8f6a9d2c6474eaacbdb1477dfc6342d827eb111f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9184bde64f75bc0898f709fdf492555b74abd3086acfa010bcd4c6dd3130ab`
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
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:e4cfa25241b18c60e1d77cc5cfae85a9e13d25b981d6592cf216e6292e3a9555`  
		Last Modified: Mon, 29 Sep 2025 23:34:30 GMT  
		Size: 49.7 MB (49736818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e573455d7fb5304cf7248f536b62a4140b90208a5690f4a3a85adc6e5547e5b`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 10.4 MB (10379740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22b291dd14f83d964b7f57044bc7f4a04295df37ba77f9fb5dfc9bb9c7de1d8a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2837bde73fa3149d81eb22fd9ff320d18a2c316af16da953569a16018bd3f9a`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c5c97b9334b4e50feeaa05190b4476afb1c64d57ae2a3336fbecf4267507ae`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 89.8 KB (89840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617c03802ed8fc2f823aeb323ee3010b4ad1f995325a6947fecb7a0a0a9461d3`  
		Last Modified: Tue, 30 Sep 2025 00:16:34 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:7a40e42eeaf5bd5622f29cb6a9dccd0f2036541929f187703eab2dcd3cb73fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3619581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3525f3a7effb0513b670c1151c6e814417883c77141c277e0dfaae15ca7ebd65`

```dockerfile
```

-	Layers:
	-	`sha256:bb336d527b6b81a8b19843c8b794c242c15418fb84454637d98af93a858b6d0c`  
		Last Modified: Tue, 30 Sep 2025 22:07:49 GMT  
		Size: 3.6 MB (3603579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e8bfedbe13e8c850a9352ab07cb8c2451926c8b22fbbef681706adcbcc2380f`  
		Last Modified: Tue, 30 Sep 2025 22:07:50 GMT  
		Size: 16.0 KB (16002 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:92b039616dcf059809b62e835c2ce1fb356f4cd490c14c863ddbb4f81570d2ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60100693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c5695ee1268cbe16821e636a6a6de9143f516e858fba50a8746679ac8c8e02f`
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
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:43c9f83b4c0cbba0c49dce5bbb999963ed78f9198001feb88e7464916cedc070`  
		Last Modified: Mon, 08 Sep 2025 21:14:38 GMT  
		Size: 49.9 MB (49863496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad7660c35dc9245a3651760544eb6d528a0717570b22435a069d38bebcd4357`  
		Last Modified: Wed, 24 Sep 2025 06:52:43 GMT  
		Size: 10.1 MB (10143297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94dd4856fbbd8812c3c3b07b916f604327d04013c0b756c50d815b3737d5a3a3`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 2.6 KB (2637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b49b1700cbeb581584f2de01718799af245efd3c1972207bb7a4cb2cd586b`  
		Last Modified: Tue, 23 Sep 2025 18:26:24 GMT  
		Size: 273.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c05e31d8c611a15105712c9f93a7d834b93de603459f204925647c9e891abb`  
		Last Modified: Tue, 23 Sep 2025 18:26:23 GMT  
		Size: 90.5 KB (90542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b573a07e48b33f323dac37694b9a4a2ac7a9be42a1d64ffe538334c6725ecb`  
		Last Modified: Tue, 23 Sep 2025 18:26:22 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:dc967d49f585f0360b55969f2a013216fab797309dfe973f1d413f39b39e2119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3627349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd6eb2694ece8d67925bc06c1ac0aa05f71d39d9a1852f52a881473f433cf61`

```dockerfile
```

-	Layers:
	-	`sha256:7f44ac7080f4f07f4a92b14c9203b3500126b0a1a15a00e395e3678201cdac02`  
		Last Modified: Tue, 23 Sep 2025 19:07:31 GMT  
		Size: 3.6 MB (3611207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b186d8b4531db4698e1f2b80fe05e77d72e2ae2c9b558c2e1e3b38bd5777443`  
		Last Modified: Tue, 23 Sep 2025 19:07:32 GMT  
		Size: 16.1 KB (16142 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:forky-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:f430324cf9cfaa124d9776470203aac188ea6774709949a77b63e213adfa7ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61745177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38ab08689612a8e95f9cc551ea0e8a30bda1c448048e882314e67c82e2d34da`
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
# Tue, 23 Sep 2025 14:32:09 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:376eb1520bb62885f5204083862e9559c55db2c2217bc7ae5d95166cd5564cbc`  
		Last Modified: Mon, 29 Sep 2025 23:35:30 GMT  
		Size: 51.1 MB (51119420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec729a899466ae066afe6bfa44772bb49f12eb1ff9130de5775863dfce2fa5c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 10.5 MB (10532172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016bd38ecc73b56e051fb135bc2f1b210de58690a65bd5202836c5e688c442a8`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b44b7f804d68298cf138540a3c3108a2814c8cc63932f7300357c68efe7054e`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e9b8bf1f68d7180b0cdf3058bac384f72680340471c2b07b70711bef9c350c`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 90.2 KB (90232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bbf84aa702d16438adb1888b29adb0d130c0a91212dad4f8842d559e332ab6`  
		Last Modified: Tue, 30 Sep 2025 00:23:18 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:forky-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3b490107fb10d10a6ec4ea0b23243b771a836b62a9ec8a2428a0dd7c4b38d4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3617512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48447039b9ee7cf8a837ef0de7f2fc8a4c3e43acdd0ac2c4ad657cbc9f7839ef`

```dockerfile
```

-	Layers:
	-	`sha256:62948bb3b9d5b778029c610a4efda1d2a480c111bf40184b640d8df7f51d9e93`  
		Last Modified: Tue, 30 Sep 2025 16:07:55 GMT  
		Size: 3.6 MB (3601540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:153eff5adb942a4269e6f4cb5eb6afbaaab407c0686fde860d67023ab18eb4f2`  
		Last Modified: Tue, 30 Sep 2025 16:07:56 GMT  
		Size: 16.0 KB (15972 bytes)  
		MIME: application/vnd.in-toto+json
