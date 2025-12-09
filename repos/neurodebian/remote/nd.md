## `neurodebian:nd`

```console
$ docker pull neurodebian@sha256:db5869b2c3206c287f97e15fefd1379c12f7fed99b2f7b9abbe1d65f13cbad9f
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

### `neurodebian:nd` - unknown; unknown

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

### `neurodebian:nd` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:2744316df78b574cddb56deb6c7b5d98809cbee4b71d6d8d5529d1a274d3371a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60215020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d877eea71086f610de199edadc40b6a55f9c29607397bbaffab73266d2d863b1`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1765152000'
# Mon, 08 Dec 2025 23:17:38 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:17:39 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:17:39 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:17:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:2e5b290b66ba04e2259d84d677cc1c79191dcc391b2b9af44fa26a4735123220`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 48.8 MB (48838607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9e09c715931d61a589379416dd78bb6256e73c88c811e500f8e557dc5ee3d4`  
		Last Modified: Mon, 08 Dec 2025 23:17:58 GMT  
		Size: 11.3 MB (11282155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc2db02bd77eab6698ece7e9df7c5b653ac5b10c08f0810cc2f43d0b3e1e37`  
		Last Modified: Mon, 08 Dec 2025 23:17:57 GMT  
		Size: 2.6 KB (2635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491ae471007885032ed5e3f28bb7baa1335bc4d41e06fe0dbdbd099dc0f05196`  
		Last Modified: Mon, 08 Dec 2025 23:17:57 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00048b32be067db84556b532031d1426a9ff788786f42e8afb936006abebca23`  
		Last Modified: Mon, 08 Dec 2025 23:17:57 GMT  
		Size: 91.4 KB (91354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d737544c398e37272ca080923473db4120b4acf0c5474006007e5b50f625352a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3606112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb817d5b7aed320476d171b96c3da8c096bc54ca4d1a3945412e96047a138946`

```dockerfile
```

-	Layers:
	-	`sha256:cc9951c3b313063bfa043b9b8454cb31d5a91c6622fc4474feaaa505240cae39`  
		Last Modified: Tue, 09 Dec 2025 05:08:17 GMT  
		Size: 3.6 MB (3592083 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b65422147e24b431af0c2bb375c2fffcc022311e69907f9bf7a82d6eab4de1f9`  
		Last Modified: Tue, 09 Dec 2025 05:08:18 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd` - linux; 386

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

### `neurodebian:nd` - unknown; unknown

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
