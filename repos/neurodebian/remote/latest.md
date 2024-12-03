## `neurodebian:latest`

```console
$ docker pull neurodebian@sha256:2f2ee431e155b1cbdf9193f76b66b200a715d206243e041e20ddc1e3ce5f4f29
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `neurodebian:latest` - linux; amd64

```console
$ docker pull neurodebian@sha256:0c7d59a5f8e1550b820a5027a093228b51c5e0d66456669e84947e7afef32a42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59859170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97157fe06be6c40ed4369da113e6278119516d03dad788264ccf1e31b0c42a01`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950a82ed7125db9e9031ce90322ac9e66a78ed9482daf60f03df07a95a014541`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 11.3 MB (11266835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1c1b38f8cddfd22a2af98cec683daf6d65d23803957e5dd5dbe69f804a2a3f`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1a0dbd43a3757bda4754fd5c0f02f8548b6030e705dbbd50eb9023dd48b226`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff386c46e5b85cf021e16c77a07eeb3acc1c69637477e33c7f2e55475483934`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 93.1 KB (93138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fbe03585af1476fb2bbd2908efaa2b8ea83b4b68bf5f6bc58ef85f1e70eefc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97ad597ee27c7c3724f6aac33bc5a022ea24f97ad9d4d365a2b6f265f19a26b`

```dockerfile
```

-	Layers:
	-	`sha256:8ad1888ebd680f37d0b7a3511d4c5b1c740b11d503c347ba76058a40d228ad59`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 3.9 MB (3937231 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86b9c5da835238bc532ec29b931a715c71c311204760c6932ba56679ca5e5184`  
		Last Modified: Tue, 03 Dec 2024 02:31:30 GMT  
		Size: 14.0 KB (14000 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:5eb8620046a2e02bee05f9dcb5abf9a7ea018cba00b6a5b19d10a4d20b2c25a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.7 MB (59653510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da76854b721e08ea18a3c19fb37d170beaeeec6f442c69d981d3a205fd3692bc`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6d6f082b94e725149735aff5f39abf2a5c1faa04f4f35829c2b04bcf36fdb0`  
		Last Modified: Tue, 03 Dec 2024 06:16:59 GMT  
		Size: 11.2 MB (11232475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7164374defb4bad306066d94c7dac571980f047bf262c550c04b585b492527`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96a1000d937bcfa52ee6cff54a54a79274765aab42bb61041dba4d40c8ea00a`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ab49634abc6db7b16ad6e4f6d1bd12260c9a0555ba2d16c5abca22782e40f3`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 93.4 KB (93363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:73fee13f802494da87f2824243b1ef6ba160c30fc88f4bb898d47172978292f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 MB (3951621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82beb41f84b93d8e674c7203b9009b5d27ade9c1eda441be5ac865312e51e9aa`

```dockerfile
```

-	Layers:
	-	`sha256:942f1434e7601bc69e26b7cade69d8c6c91abbc09905aa7e29e161a332fa32cc`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 3.9 MB (3937484 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a95f2482d505abe9ca79152c5fa27d45a5ecbb3e300f19487154106eb2c2a20`  
		Last Modified: Tue, 03 Dec 2024 06:16:58 GMT  
		Size: 14.1 KB (14137 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:latest` - linux; 386

```console
$ docker pull neurodebian@sha256:7be9f025a968af1334c291d8942067638fecdb9ae6aa2e02ac3a5409c41a37a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61260403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd04204578e3c76cda4b47577a26bbace9322f371a285123aa1fc902be6a98a1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 21 Jun 2024 21:57:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian bookworm main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel bookworm main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Fri, 21 Jun 2024 21:57:43 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590fcc30f6c50f7ad71c3858d2239c46376094eaf1a12e0ef65a4673f5e763d5`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 11.7 MB (11689045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fbe2a76c7a0519eb8d714422348d7d6285bfaf0888b3d5341e0bc6ceb17e999`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 1.7 KB (1740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75487833f3368eab2257a94a630b1880b487a3d9c985df44821377679a8630bf`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7d9d4001de6a0138bedcfe6908f4c986a615e32193ee3c092897d30647ed46`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 93.2 KB (93219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:latest` - unknown; unknown

```console
$ docker pull neurodebian@sha256:44e8730314266bff6d4bb59854d8785f0f8fe79a8da4a423ce7a6886f9fa63cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 MB (3949114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb443803c49e4d4189b2e400064620236d7b0aba3972dca81fa2dd4b2e294c5f`

```dockerfile
```

-	Layers:
	-	`sha256:84859747a36c49bfba821a162fe221c7cfe11f09235d8f7a8f66c8c32748ab80`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 3.9 MB (3935148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b7067294bc3a8508f9cb372c5d48b39df12f9b701bafa3dbd11218ff8555282`  
		Last Modified: Tue, 03 Dec 2024 02:14:53 GMT  
		Size: 14.0 KB (13966 bytes)  
		MIME: application/vnd.in-toto+json
