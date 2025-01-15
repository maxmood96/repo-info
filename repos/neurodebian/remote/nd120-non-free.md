## `neurodebian:nd120-non-free`

```console
$ docker pull neurodebian@sha256:62a498bda9d1eee73ac43908fd8131ed62996a164295d3bcf2888b2164fbc780
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd120-non-free` - linux; amd64

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

### `neurodebian:nd120-non-free` - unknown; unknown

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

### `neurodebian:nd120-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:0675849061bda1b38185c2e1812d727d5b0d1db5ae8f3c09181d39f227ca47b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59635086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d0eb33669da82633d048e56398d2ee12cca1688105f20aaecf564a63e1f25b`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:e474a4a4cbbfe5b308416796d99b79605bbfad6cb32ab1d94d61dc0585a907ea`  
		Last Modified: Tue, 14 Jan 2025 20:33:16 GMT  
		Size: 48.3 MB (48306896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63297db49aa1fee77d18a7f692b7b36f85214cbaa7f8a77e111f638aea5edbd0`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 11.2 MB (11232397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30096a8bba85c4ddea6082a5ae4d246978818eb34e1a6355eb305dda4439e502`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d9ab318aba0ec0653df3f41df8255bcf221a39e34c2e6e6bcc9f0b537063e7`  
		Last Modified: Tue, 14 Jan 2025 23:34:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986c7651cc110568cd8c25742246a21c09c882a240da263ec1da9e18328d304f`  
		Last Modified: Tue, 14 Jan 2025 07:29:59 GMT  
		Size: 93.4 KB (93378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b55876296936d652efd807c401513a3d8dd9ac97cf2648dbd96a596ef9b97f`  
		Last Modified: Tue, 14 Jan 2025 07:30:22 GMT  
		Size: 427.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd120-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:639b93a3d0a313aaeb9b27ca2dcc439bb59d78547e5f285cfe9414b664382a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ab937b993ca5d9b3bcff1bec8f89c63b742ee19d86fe582f2487dfa6468594`

```dockerfile
```

-	Layers:
	-	`sha256:fd87584336d0bf806432fe2e706599ae36e1fffe26cd0655465d6c421edcb895`  
		Last Modified: Tue, 14 Jan 2025 07:30:23 GMT  
		Size: 3.9 MB (3933104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:702c5a800583ddff468432d35aa75855a0c9a8bd4961e8158cf542f3b265fd3f`  
		Last Modified: Tue, 14 Jan 2025 07:30:22 GMT  
		Size: 16.2 KB (16183 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd120-non-free` - linux; 386

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

### `neurodebian:nd120-non-free` - unknown; unknown

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
