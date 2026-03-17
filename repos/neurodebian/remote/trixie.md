## `neurodebian:trixie`

```console
$ docker pull neurodebian@sha256:fe3b81e04ddaa8fd78726011a91d9f0f3f695fa07219d8ac602692a403a1cc04
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
$ docker pull neurodebian@sha256:38823791da050edc5eb8f6fa536c491e2c8ca8005a8cd254481432b3141a3c15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59683732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6669aa02982813b549bb24f0efb1f87ca6a0a484f7104aa429108da356fa2a73`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:41 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:45 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:8f6ad858d0a46fa8ee628532c70b8dc82d06179d543b0b09ec19fc03d4c5b373`  
		Last Modified: Mon, 16 Mar 2026 21:53:17 GMT  
		Size: 49.3 MB (49297530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ee88a3265bdb3d0530757a6461555d707868eee596f1f998298c190e3f644`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 10.3 MB (10292915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef101ccc9e6d95edb0e8ce65d3ffc82d69cd46fba656e62ca670d99e42249eee`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e923b7d0ba6be692a9bd27955a6d7d130f86d66f9bd9df859a7f4be07e7087af`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e64cfd12a5f906af9cbc34e19af3580efa8f976499c5ffb3c985c022c8e508c`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 90.4 KB (90385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:85b2232400c1f431ba8cc26424452df9318c1b02c53f299adf17432331fd5610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3628354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd9443133cc72a0d386f5b16557cb5a52932d2afee8c29b96f75ff0e5d8423b`

```dockerfile
```

-	Layers:
	-	`sha256:a6a58199c85a0132c55237be5d7d27187876d7ee3f1416b14fcaaa1cc7ee98b2`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 3.6 MB (3614104 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e73bd9c5a29d25f9da77b0fedb2979737b707d74c6ae43bad84b50e6e266c99f`  
		Last Modified: Mon, 16 Mar 2026 22:44:52 GMT  
		Size: 14.2 KB (14250 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:901b7b25ce96aa90447603c3515149806a5d64a7cc6e67690efb485ce28b27a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59836813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7795498bb7dbd01166c2b326da248bbe4cc5d0d490ea9050315b99c8419dc1b`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:46:50 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:46:51 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:46:54 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:deab8db42772fcfeb45003461fe0eb7bf63bdb29199a4fb76242b9493437c28b`  
		Last Modified: Mon, 16 Mar 2026 21:53:03 GMT  
		Size: 49.7 MB (49664953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df775a7faa43f7f7252f06117029e4dd5a5cbac50c51890b0d6d3cfd8405b0cb`  
		Last Modified: Mon, 16 Mar 2026 22:47:03 GMT  
		Size: 10.1 MB (10077947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58a0f5113878ee3b18eb8ee6a2439cd3d4c0311b4a2b783a57ae7f91570cc26`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 2.6 KB (2632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b5bbcfe31d9f345176f105df35710778037261c4780ab6b5767185e16411b5`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d101e6915fa0def37b1a745ea4ff99954c71a09f8a1d36fba13a830235ee2f37`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 91.0 KB (91012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:600774acdcdbba3fe13459a4441324f1c491857eabc5df29fc63bd89b791f89c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c9030a439cbc6343ab6e5529fe5513af33f6a1ea35920d12615cdca32dd0fa`

```dockerfile
```

-	Layers:
	-	`sha256:8a045eefb957935b32df8b5f3f9841257d01411ae260d6403aa68ab7a16f082b`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 3.6 MB (3615631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb422972c47227f8b51f38ac744f2746fa68bd8246da0bdc0c4a0369275bebfe`  
		Last Modified: Mon, 16 Mar 2026 22:47:02 GMT  
		Size: 14.4 KB (14388 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:trixie` - linux; 386

```console
$ docker pull neurodebian@sha256:ed5f194f7c2abbaae636062e9e03e383495555d870ecd8a7a204c6ed0031978c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61379608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23b782793b45d233eb4c1cb7011a7c66e56885f7e893ff51d4360c3b1dc6c82`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:44:54 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Mon, 16 Mar 2026 22:44:55 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian trixie main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel trixie main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Mon, 16 Mar 2026 22:44:59 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:a59dab062b6e61bf7c8c44e3e14585d36526de4560825ba7d4c8196503c6eb87`  
		Last Modified: Mon, 16 Mar 2026 21:53:40 GMT  
		Size: 50.8 MB (50818792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e327d8697f911e128822f25c7c3a0b25075fc412d07427074366c4a1dcc06c6b`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 10.5 MB (10467149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa825e034237965757272c1d539290ce5f98985c6f606968b5a15d07e4230c97`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 2.6 KB (2636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf20d220105eee5bb027f81176948567b8ebcf7b0d3e64a6f976fed93b757696`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2929ff200bd80db2d78e35ec44a161b98776d7a2a1f0470e391c0712e3e5e1e1`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 90.8 KB (90762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:trixie` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4088065eeaf99003a949cc4c86cdbb851614c39f97e157c3e608533525003145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3626270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973923d9da01f833bac03850854ab5ff2f09f4b5440e89c3cfb9351a84d2a6c1`

```dockerfile
```

-	Layers:
	-	`sha256:0e6bf81854fe1d14a17ca159eb87e1f89012c8acbbdcf6c314097a44fcc1ad9f`  
		Last Modified: Mon, 16 Mar 2026 22:45:07 GMT  
		Size: 3.6 MB (3612052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60759a73115e1d8354102c4f15b6ca89c3ff7e7c3ddc0140a9e3ae91e615ff78`  
		Last Modified: Mon, 16 Mar 2026 22:45:06 GMT  
		Size: 14.2 KB (14218 bytes)  
		MIME: application/vnd.in-toto+json
