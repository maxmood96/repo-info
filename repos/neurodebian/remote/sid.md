## `neurodebian:sid`

```console
$ docker pull neurodebian@sha256:86a955a6da2fd6e49310005ddd799d6d0c1b03e61ec3a26bf798c7e17fb2dd88
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
$ docker pull neurodebian@sha256:742f81326d6458fc4835788d8fe3317f77b687290629fc738389f12c4814df3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60288474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13d9d256c1ca3e4c144c863cc2281316c3cc3eb45088369a88aea3a40a0914ef`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'sid' '@1769990400'
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 02:49:09 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 03 Feb 2026 02:49:10 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 03 Feb 2026 02:49:13 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:e5dc831051d738f5c1db4254dde56feb7c9e75e136e23995d896f1b6e1ba752f`  
		Last Modified: Tue, 03 Feb 2026 01:15:47 GMT  
		Size: 48.7 MB (48654703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84911d1558a1b3010131d47ee741db0963c889273e31e2a95035fd6cfb9f17c1`  
		Last Modified: Tue, 03 Feb 2026 02:49:21 GMT  
		Size: 11.5 MB (11540410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582397b9dc850b850ffd74061feea99dfb6b237c0192d6191177bd0a6cd86b64`  
		Last Modified: Tue, 03 Feb 2026 02:49:19 GMT  
		Size: 2.6 KB (2634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6309d0a7b6729391c7f1314a74b6b06b07c4646ed52a3d9e7ce4cb11daa5bc`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0740384dd13f89422fe1f4638c08fb758dc33e4f5c9810aa0b1d0a69d7fae0bb`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 90.5 KB (90457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:4e1ba3408ddc3dfef56dc25b1915ff61fc917b613ede0a431592467c4b4864a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3621565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba3eb40824aca52a92259785bc8cb173186a6bb1ccb406742f34f2f6ebfec74`

```dockerfile
```

-	Layers:
	-	`sha256:7d69e622a5bfed66bf691b20cdf1aa82f53f6f580b821ab40aec94be47d4d4b1`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 3.6 MB (3607661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed7e7edca04a0e1aa36eebfdd3e3f3946a1ce7603207a77681ec83592f931e12`  
		Last Modified: Tue, 03 Feb 2026 02:49:20 GMT  
		Size: 13.9 KB (13904 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:fa0ba41b4e84d980cdefd58691824eb67a3c89e5ce751baafa6676d27374880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60202507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e98d5b725f75bacf9154914537830dad7da7c50305e6a09d608433860d4f0361`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:38:03 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:38:03 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:38:03 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:38:07 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:6d947e77c03f512510d8bed1eff4f80727f54732f6ae212199524bdf89493609`  
		Last Modified: Tue, 13 Jan 2026 00:42:02 GMT  
		Size: 48.8 MB (48824718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da01bcf829ac0481e16c259eb82b33f353df66d362cf4da5276683b0b2b9319`  
		Last Modified: Tue, 13 Jan 2026 02:38:20 GMT  
		Size: 11.3 MB (11283991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b508d27ae81a583413ba342757fe3a8e81b34b43dcaf3cada42f01296b880433`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb85291bd22f4f2d342b547834f90db0ef1315dc5b3db25f80d522429c600b6`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0758f88b1ad03441d33efc0759464c7090116fd1b6225e6bb3549fba6af4c928`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 90.9 KB (90900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:fd4287db1c80d84718a24bbf7b419272c01514b21c14f2017321173cfbaf6ce1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3608098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6178646fb591280a4322dda9041233d675f14ba891bcf3c3cdb42b6669a33488`

```dockerfile
```

-	Layers:
	-	`sha256:0827d76799ed2ee2ffd22bb96db6c785e7ab0c7910d70e72af72764c15894510`  
		Last Modified: Tue, 13 Jan 2026 02:38:20 GMT  
		Size: 3.6 MB (3594069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:079930c725e760d95d23f7f8d75cf0c97b6bb6f92cd6ee6185135a9359b10eb9`  
		Last Modified: Tue, 13 Jan 2026 02:38:19 GMT  
		Size: 14.0 KB (14029 bytes)  
		MIME: application/vnd.in-toto+json

### `neurodebian:sid` - linux; 386

```console
$ docker pull neurodebian@sha256:75cfaf1c6b7dc32eea6e9ad0986a93ef5eeaa1ad62b6eb7b9b92c50a27cf5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61815161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:619842c0a344cd4cc323e6bce0195b699ffcec1e1e11d144aa7ba65e03ae8e4f`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'sid' '@1768176000'
# Tue, 13 Jan 2026 02:14:44 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 13 Jan 2026 02:14:45 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 4E9A2E702A23C7C882574536439754ED1F42AA2C 	&& mkdir -p /etc/apt/keyrings 	&& gpg --batch --export --armor 4E9A2E702A23C7C882574536439754ED1F42AA2C > /etc/apt/keyrings/neurodebian.asc 	&& rm -rf "$GNUPGHOME" # buildkit
# Tue, 13 Jan 2026 02:14:45 GMT
RUN { 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian sid main'; 	echo 'deb [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian data main'; 	echo '#deb-src [signed-by=/etc/apt/keyrings/neurodebian.asc] http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list # buildkit
# Tue, 13 Jan 2026 02:14:48 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/* # buildkit
```

-	Layers:
	-	`sha256:621ee2827046628793df0c5176988fc0eef90eb94ab1b862f17e074ba6064e3d`  
		Last Modified: Tue, 13 Jan 2026 00:42:41 GMT  
		Size: 49.9 MB (49943816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37772ef8b09ff9ece288ef28843ba2b28651580cfaaa82c9376253b633ebec17`  
		Last Modified: Tue, 13 Jan 2026 02:14:57 GMT  
		Size: 11.8 MB (11777889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b62c15fbf7ad5a88504652ccc590c41168dd750ad796ee00cb146201e51d41a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 2.6 KB (2631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572d1ccf01b56f7a38834164db204119048dc7f9118850e151ee844646faa2d7`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcc6d97bb71fa9592ffbe96f2e81728683ccd72aff6a26e2a3dd0b3342b417a`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 90.6 KB (90557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `neurodebian:sid` - unknown; unknown

```console
$ docker pull neurodebian@sha256:86bbfdaf6aa29318b32ef02597c6614d32d58e53aba363eaa8a6c80a860a36fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3605027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109185c65d9918c90b219c20784cc9ff1d784bd8e3c7eb098dd0571837b25969`

```dockerfile
```

-	Layers:
	-	`sha256:b48b602aa44be33ca0546314de063837fef65f8f602a6f9a01c8ec2a16fe31a9`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 3.6 MB (3591151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8768990e2a7177e584c19848ea859a7128c68a9856c85d9b11594e75f37bada0`  
		Last Modified: Tue, 13 Jan 2026 02:14:56 GMT  
		Size: 13.9 KB (13876 bytes)  
		MIME: application/vnd.in-toto+json
