## `neurodebian:non-free`

```console
$ docker pull neurodebian@sha256:e74df4c5ea434d10ff72a92ba8b5d8f42e72d9e2f0f7b038779916c0fc4a8e50
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:57dc4c223385bdf9dd989688345326effd26cf63a956431eb3458d862e893538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59842295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89f3233916c97ce00f4022ab1000031c5cb1165d2cbd78328529fdc3f47e946`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:fd0410a2d1aece5360035b61b0a60d8d6ce56badb9d30a5c86113b3ec724f72a`  
		Last Modified: Tue, 14 Jan 2025 01:33:18 GMT  
		Size: 48.5 MB (48479962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d7bad9e0da2b69c02e2961fd5b41ec0baf93ece5af0fe4e4d2b4b3c194559b`  
		Last Modified: Tue, 14 Jan 2025 02:35:26 GMT  
		Size: 11.3 MB (11266788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96125b71f05f6a267733ad919d02c18052dd7050d6d265236c799681e2e6b98f`  
		Last Modified: Tue, 14 Jan 2025 02:35:25 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25edc150705b8cdad76c1b1a8c9545e83967f17674737e966f61ed2975693f91`  
		Last Modified: Tue, 14 Jan 2025 02:35:25 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226b26042ffc15688dbdb3e63f12171a1ab0505ebec1ad9a1878c1b9df5175c5`  
		Last Modified: Tue, 14 Jan 2025 02:35:26 GMT  
		Size: 93.1 KB (93131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9389680a8bca55ea1e51e85c35a9c8b24d4029741922a08d948cf8d067e86cc2`  
		Last Modified: Tue, 14 Jan 2025 02:35:26 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fc34b2dd85e9f01fab5465ab2f87a3dcd226b9e9e3dd67934a7ff3c252b726e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3948881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96c1fc754675848c93ae4ad08c0f1a0fea34f406d29830a87c21ebf460d72d4b`

```dockerfile
```

-	Layers:
	-	`sha256:a8ced2ce53d1cad690e9ac809ce96f49c4b3a5666da812164c3f8db7b7c497c6`  
		Last Modified: Tue, 14 Jan 2025 02:35:25 GMT  
		Size: 3.9 MB (3932850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:788fa9d60d38f1421f63329bc21fbaf8d75040c7276a9c31649d4c038a886a8e`  
		Last Modified: Tue, 14 Jan 2025 02:35:25 GMT  
		Size: 16.0 KB (16031 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa97feec1d4944ff4684fa7ec8556f425fa31a11c10de0e0791700b8d8df1101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2577dbdb1d1713f34148796b855dccfb4c136e1de53881ff63bfb66b932eb15f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0367019e15543f02a69e834f1c24024f42ff4a354dc1d505f1fb3f7f641f344`  
		Last Modified: Wed, 25 Dec 2024 02:19:39 GMT  
		Size: 11.2 MB (11232347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a91a2c5dffa6242c8635282e5d3644e5542d4d3fa55a50296ad77f135894427`  
		Last Modified: Wed, 25 Dec 2024 02:19:38 GMT  
		Size: 1.7 KB (1743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f7a3036299a2c5f2be4ab8d3c47a46eab3f06d55ab60826cc639ced1d6c067`  
		Last Modified: Wed, 25 Dec 2024 02:19:38 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06582c2036bcbd28dd303ac041a31fa9d209a44ef50795590fe9abd81bb38db7`  
		Last Modified: Wed, 25 Dec 2024 02:19:39 GMT  
		Size: 93.4 KB (93405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea873f9506330dd9096c06c86ddf5aeae6dfe621dfcfb5960765ec2c9251a95`  
		Last Modified: Wed, 25 Dec 2024 02:19:52 GMT  
		Size: 428.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:d450d31baf94e8405e36a31eb7e9b2c2dee3fcd5d08f4f68f25ff6a0e827faaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bae39e06a4ad965359f8e2212ab571a45be9a5c5956670e173bb3dbc1063be0`

```dockerfile
```

-	Layers:
	-	`sha256:8f3b70b147c37ed8d6c99456de344fb2031278ae354f9c735dacbb5088f512d5`  
		Last Modified: Wed, 25 Dec 2024 02:19:53 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5d99980963c9a4ccf630c30593aaa1b2ca192c6318ca07d627096ff1744aeb9`  
		Last Modified: Wed, 25 Dec 2024 02:19:52 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:c617f4c5b05d1a14a5a85403f83944aa959bf0bdddb82889f52465868f3d64c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61242312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85e3db6991271c9025b627634d77ec55c8af2c56441a0f738a7b9cff31b100a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:46529f83455afa979c42fcfe436f7b07f4eb4d873a153eb3dcb49167de675239`  
		Last Modified: Tue, 14 Jan 2025 01:33:29 GMT  
		Size: 49.5 MB (49457745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae4673bb1dec4128030db5783cb766d03834afe9894bf9f919a52e2f84d5dfbd`  
		Last Modified: Tue, 14 Jan 2025 02:17:59 GMT  
		Size: 11.7 MB (11688912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c710fd3e5f37fac1481b6396ce426af65c4ac15278ffcce1eeec8ac99e662a7f`  
		Last Modified: Tue, 14 Jan 2025 02:17:58 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c9dca3d5cd27acf40a29b7f86f60d1c3b54587ca9049b7efac2e104af5bc147`  
		Last Modified: Tue, 14 Jan 2025 02:17:58 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f4dc5f04985d6890d3009a6bcf340ded20a09959457723dbeb6e90a0c44e41`  
		Last Modified: Tue, 14 Jan 2025 02:17:58 GMT  
		Size: 93.2 KB (93241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153454a0e2d5a445c1fb3196433c5c62c373ec51cd8f8060be3889d8c378a25b`  
		Last Modified: Tue, 14 Jan 2025 02:17:59 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:e2b1864d92d7c1efaa15a107e7ba42ebe0d38744813196a7670b7740f77456d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3946763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be0e111efa67740865910bdcea0582f69a6dd3b0822a866fa1940d66e231d26`

```dockerfile
```

-	Layers:
	-	`sha256:de29c8ec819b9c69508596111ef6b55ab236d95626377562fe6ba6a3488b87f7`  
		Last Modified: Tue, 14 Jan 2025 02:17:58 GMT  
		Size: 3.9 MB (3930767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b26d6019be8383efec58b222fae1a79133eaf3c985727fabfba1d1f23dc6381`  
		Last Modified: Tue, 14 Jan 2025 02:17:58 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
