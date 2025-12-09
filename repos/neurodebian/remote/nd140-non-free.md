## `neurodebian:nd140-non-free`

```console
$ docker pull neurodebian@sha256:e7cfc622f46a812fa7cfbba9c6deb28a746c15e45cec5c9848e0c0dfc14f5bc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:nd140-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:7d52b67a4052b95da77b50bb5a94b250809f461f5fc6d69de6dbc1b67acb1538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60209690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09a1044fa869c8749314dfda658c9fa02de5cc0d3b87e922d67f2cd405aba61`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:13:59 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:13:59 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:13:59 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:14:03 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:14:03 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:c7cbbee3050ecd826301596e459f3fa12ca32f5ba2b65d33b56172341d2cd3ff`  
		Last Modified: Mon, 08 Dec 2025 22:17:14 GMT  
		Size: 48.5 MB (48512511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f88d3ce54e78af814695ebface377bb0ec3487056a2eea2aee7897a603e560`  
		Last Modified: Mon, 08 Dec 2025 23:14:17 GMT  
		Size: 11.6 MB (11603244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9831661f90e1fff62770d0557d889d93bfbef62ffd537a209035ccf3fd34e0dc`  
		Last Modified: Mon, 08 Dec 2025 23:14:16 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95de12d576974a12a6931a581828670b438bb7ab75f84e8315b9ab58a45dd7c1`  
		Last Modified: Mon, 08 Dec 2025 23:14:16 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84de5a89ba5144e5c96c9dd599cc50792d3d8177db8cc686e5d814f22e6c1831`  
		Last Modified: Mon, 08 Dec 2025 23:14:16 GMT  
		Size: 90.6 KB (90585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531243e1f03fec8ab2c64e577a2fd634c765f67a587a237f3e0d0782de0fe4fe`  
		Last Modified: Mon, 08 Dec 2025 23:14:16 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:29a851096f68da93456f8fdc5648546924969dc105f675329785f9dccc66411f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3601573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7bf348e748cfc25e6f065d5068f99bdbb6f6109fc0cfdf24d1b2b440948e9e4`

```dockerfile
```

-	Layers:
	-	`sha256:30793f141f81991ba970f93e5f6ba6e09d4e94d56c43f4370bcc7d35ede91f85`  
		Last Modified: Tue, 09 Dec 2025 02:08:12 GMT  
		Size: 3.6 MB (3585614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90637bd859a9008031ca0359f7ddfded0615f08d70287acb20a29142eb888d95`  
		Last Modified: Tue, 09 Dec 2025 02:08:13 GMT  
		Size: 16.0 KB (15959 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:d06aba823eb1b4ee0a1a7a91c948cbb6988fa7f7a7479f38f9d4b81212f479b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59964769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a41e9d8cf8900e06575b95d7c01f32553609888d586a19b54771fa344d4a42`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:17:28 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:17:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:17:28 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:17:32 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:17:32 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:60db063fe1f6101cd454be84b0b672c499625ca27e05c40ddaf285db3af29997`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 48.6 MB (48599337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74f5f709daddf62de01d0b33d59473358394c568436196e1b44c00e23470e68`  
		Last Modified: Mon, 08 Dec 2025 23:17:47 GMT  
		Size: 11.3 MB (11270845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460eab85cf76811ac700f082fe757767b81f50a9a5e66235d44379eff1c27dd6`  
		Last Modified: Mon, 08 Dec 2025 23:17:46 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e73ad3d080e57eb38448fa1e73b25682dc10a747f775a53e64af499a4950e9b`  
		Last Modified: Mon, 08 Dec 2025 23:17:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c10610d95db915ae3b9125a42d20c6b3908153acddb32cbbd278bddf59def1`  
		Last Modified: Mon, 08 Dec 2025 23:17:46 GMT  
		Size: 91.2 KB (91238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9801fe5f03aab288259a41ea2568737965f0eadd8639ff34528bcc006fce6a61`  
		Last Modified: Mon, 08 Dec 2025 23:17:46 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:b4a3015c901a40498c3b227fcc8ce97dd584da3139f180e3844edd2f88389170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3602589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebab9c3d6efc686b457970a80b88327d7b089b2c4f34087105360bc05e324550`

```dockerfile
```

-	Layers:
	-	`sha256:a4bf256366b1929bf66cff57d9995be250fc80bc397dd7f9b08dba19fb72709f`  
		Last Modified: Tue, 09 Dec 2025 05:08:05 GMT  
		Size: 3.6 MB (3586490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:028d7451aaed3b5402879c84b00d5e03f20aa14740a83c68d8351001840e33c7`  
		Last Modified: Tue, 09 Dec 2025 05:08:06 GMT  
		Size: 16.1 KB (16099 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:nd140-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:310986ea6782ef724d41e8f67240e005c3c0fbfe36d6e9779c703452978b2061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61721053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75690de1cdcfaaa39c9be4ef65273d76e990e6fab068d68efa4f94bb0ba85995`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1765152000'
# Mon, 08 Dec 2025 23:15:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 08 Dec 2025 23:15:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian forky main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel forky main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 23:15:54 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs # buildkit
```

-	Layers:
	-	`sha256:a5d3e60f8c1eac1ccb5aac1ab5735dd586fe448287d7c7d1d7f59a687bd9b9b1`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 49.9 MB (49874580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ae4cf933beea0d74190c5108f5592160b361455d8d0aca4852d56b28f1816ec`  
		Last Modified: Mon, 08 Dec 2025 23:16:08 GMT  
		Size: 11.8 MB (11752199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69195fca673288bc2be238012fb534a989339e533d6a8f67d5d4ee43d28117d5`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3571e3ea3babea5298321571e0ecff849e4104964f3e97b88921df3717d1aa`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d10761b27d78d3cab80c345eade32d07c1317137a5ae92a9998e523977655ab`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 90.9 KB (90921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd6e1907cacf4ae722d1b080f12e49ca31d368e482e1835e219185719e6c1090`  
		Last Modified: Mon, 08 Dec 2025 23:16:06 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:nd140-non-free` - unknown; unknown

```console
$ docker pull neurodebian@sha256:3638e2924b6b21634a03c10613ef941641ea6b6d835763bb584846dbb4776e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3599496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9d1adf120a2f484750d4044e9113b7a12ad4287c721ee006427934f80f2ef3`

```dockerfile
```

-	Layers:
	-	`sha256:536b0ea1c809e7d334f738198e24640d9fdcc2284f7ea5394d9ac75a89aa1e12`  
		Last Modified: Tue, 09 Dec 2025 02:08:21 GMT  
		Size: 3.6 MB (3583567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1afa97a40023bd48ea41bef0a9c7435b97b608551dcbf15388b584d2047e4326`  
		Last Modified: Tue, 09 Dec 2025 02:08:22 GMT  
		Size: 15.9 KB (15929 bytes)  
		MIME: application/vnd.in-toto+json
