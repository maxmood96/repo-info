## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:dc4c155f32a23e4a6737b2aa16432edd3c30cad6a5e1a61c643293561c8d2e5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:sid` - linux; amd64

```console
$ docker pull neurodebian@sha256:b93e279d42e366154e159f24bb8f1aa31eee3d5a5cc71156672428b73c013c38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60534099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e9e911953e137448ab7807260cc45782fefde32b282b3f2fcc04edab3dd0299`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:13:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:13:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:490e982b5e2060f5a5ea7e5f586ff8bb98bb61a953b4473631a9da94fd85fe11`  
		Last Modified: Mon, 08 Dec 2025 22:17:59 GMT  
		Size: 48.8 MB (48817523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c277b03c03ccccb25311438be184000af1d4b31cb6fa5864d52e0defab9ad55`  
		Last Modified: Mon, 08 Dec 2025 23:14:09 GMT  
		Size: 11.6 MB (11623019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2802c6dad200337fb086f0fdcb89a5ed63ceb552df7109caf854e92fcd4aaa4`  
		Last Modified: Mon, 08 Dec 2025 23:14:09 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2691dc2cb76b74c1c9e367c6ffe6f83fba7ab9d01068b309b32c8b2db58fff30`  
		Last Modified: Mon, 08 Dec 2025 23:14:09 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8f026fb8db7a0afe3ab6b03373693ad1f93688fae6ed8b77c2106cebf1478c`  
		Last Modified: Mon, 08 Dec 2025 23:14:09 GMT  
		Size: 90.7 KB (90655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:230e09b5c815338e20412161376fef0479b645da897f89f753fce22810d1bd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8331cf18931a82dd353555ae60d9d6ccd69bf9dc833f75229b457f63328fb425`

```dockerfile
```

-	Layers:
	-	`sha256:78b22491c302de211f21416c7df01f15c75ddd28d58bd1824621bf9a73327b25`  
		Last Modified: Tue, 09 Dec 2025 02:08:31 GMT  
		Size: 3.6 MB (3591207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bed6e1fd4a6f9b16b6a7610b5e71ece69da5253215c84fb6678e3ca42981283`  
		Last Modified: Tue, 09 Dec 2025 02:08:32 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:541357f0ecf1813a8cbd720ff8f96f2cd982d89fd4bc89827c69d551b0163a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59940394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45372882da5d68ae7df8f8d65d5521dcd46ddef2d90a0366725a381de0b94cf`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1763337600'
# Tue, 18 Nov 2025 03:56:06 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 18 Nov 2025 03:56:07 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 18 Nov 2025 03:56:07 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 18 Nov 2025 03:56:10 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2b90f6fb16dc868101354a233036d6d70e13cd3477e4df5ab59f2ccc8607c1d4`  
		Last Modified: Tue, 18 Nov 2025 01:13:53 GMT  
		Size: 48.6 MB (48591389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2c0b4f8506d03d13edc8f4045814717acfb0bd4cc0328aae44b4d8f1bb7d1f`  
		Last Modified: Tue, 18 Nov 2025 03:56:30 GMT  
		Size: 11.3 MB (11255621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02b54aa8ab0ab54e708c0c245ecdc268d95f50763ee5e6a6ed6a4adb1d2b80c`  
		Last Modified: Tue, 18 Nov 2025 03:56:31 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137f7f093c10ede28087087e92707167136eed0692d4cb8a57ff45159fe7ab43`  
		Last Modified: Tue, 18 Nov 2025 03:56:29 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2204582058e6da481caf8d806747650c50de23d03051094ad0639f303ac14315`  
		Last Modified: Tue, 18 Nov 2025 03:56:29 GMT  
		Size: 90.5 KB (90480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fde860d58516366ee33015d1436096dd5e23e8f17964da184f085573fd9cc39f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3592300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3ab53141102408437089c3592249acd27598f72cfda4ae449b0b6ce85fc3a7`

```dockerfile
```

-	Layers:
	-	`sha256:3124dcc841b669bd8bed1254d0af82173424f14bc28093da966b9fa449b12735`  
		Last Modified: Tue, 18 Nov 2025 05:09:40 GMT  
		Size: 3.6 MB (3578271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2859914cd0af245c67d2aa284e5b6e40a46c065c99688f18da5d11a1320ce86`  
		Last Modified: Tue, 18 Nov 2025 05:09:41 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:8f5cfc00500cc0d446db7aa634f75cf84b12afe95e95ebdb31af23e36dd652c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:574cb528275d8e08c0c2aba8f98ebea411e3d9e83b8666ec032897e9890a4e3b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:15:58 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:16:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:67f7fae0ea3bb931c627a66604e60b0a242047b0c8f9186d188cf96e0133593f`  
		Last Modified: Mon, 08 Dec 2025 22:16:33 GMT  
		Size: 49.9 MB (49947966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0266c0513022413f6a42ac8de173ef0db6a7fd70a6d1859fdaee0ff7c1f1a52`  
		Last Modified: Mon, 08 Dec 2025 23:16:17 GMT  
		Size: 11.8 MB (11771438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54d5b89513ee9aefb4cbaeb149aac108b65168fa8016ced6820617134e33cc7`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44066a3eb12e5a62aeb429ee8e2fa4e039a016510b0053f5b6d5a21937982b57`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469a39499ff4a4700821efc8a4595a0a54ee4dd2c440d4d7d1bd6a635aeb8f41`  
		Last Modified: Mon, 08 Dec 2025 23:16:16 GMT  
		Size: 91.0 KB (91009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:683dbe22bfe3d344489dcd587c30032ec24bcc1eec3ddd9dc64298a5a3b44fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3603037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d30d3a82ccd78c8e1f82eefd7dd5e1a1c671e68a0c3acffd7baa9d15c330adc`

```dockerfile
```

-	Layers:
	-	`sha256:61532c3563e04ec54407712519658270da6406a9e32a333a448571a3a74f36e1`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 3.6 MB (3589161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce849a1ac7c09b2ee06fbd7089981ce600c9dc4944c42e11cbeaf60a93c90dbb`  
		Last Modified: Tue, 09 Dec 2025 02:08:41 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
