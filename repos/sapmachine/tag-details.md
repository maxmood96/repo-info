<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.14.1`](#sapmachine110141)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.2`](#sapmachine1702)
-	[`sapmachine:18`](#sapmachine18)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:6d40288661c097d2462acbae09d7b3dccbe0105bffe1c337a25c8e25d2eb92dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:8718c5ac978e9bd123ffaa7b78b0042555871c32696b8fe2e1d708e05026fdcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234595310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd949bdaaabea77d0fc8089d6c08e56a6121d7d1061d6bf15d325f198e179b7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.14.1     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 06 Apr 2022 04:15:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbd16ff38383c60b8fc1bf647050936263de1dd59479348cbd39aa26485b59`  
		Last Modified: Wed, 06 Apr 2022 04:16:51 GMT  
		Size: 8.3 MB (8317679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24060e712a80036e70b0c41da5d08017d1b47fcd2b7660b78aad24452bcd270e`  
		Last Modified: Wed, 06 Apr 2022 04:17:04 GMT  
		Size: 197.7 MB (197711339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.14.1`

```console
$ docker pull sapmachine@sha256:6d40288661c097d2462acbae09d7b3dccbe0105bffe1c337a25c8e25d2eb92dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.14.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:8718c5ac978e9bd123ffaa7b78b0042555871c32696b8fe2e1d708e05026fdcd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234595310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cd949bdaaabea77d0fc8089d6c08e56a6121d7d1061d6bf15d325f198e179b7`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:12 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.14.1     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 06 Apr 2022 04:15:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbd16ff38383c60b8fc1bf647050936263de1dd59479348cbd39aa26485b59`  
		Last Modified: Wed, 06 Apr 2022 04:16:51 GMT  
		Size: 8.3 MB (8317679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24060e712a80036e70b0c41da5d08017d1b47fcd2b7660b78aad24452bcd270e`  
		Last Modified: Wed, 06 Apr 2022 04:17:04 GMT  
		Size: 197.7 MB (197711339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:fa3118e456ff81dddf9513a111384fc9955de6d9d35e158395bae1934f9092df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:ace069bdddbd2ee49cfedda09056f8050f987394648b5a7394b9b0a47d86e49d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ed4b908a9544cc218e608a334742a506733f96b2e0e2793b53a9280e5062`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:31 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 06 Apr 2022 04:16:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbd16ff38383c60b8fc1bf647050936263de1dd59479348cbd39aa26485b59`  
		Last Modified: Wed, 06 Apr 2022 04:16:51 GMT  
		Size: 8.3 MB (8317679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7512af92b6ae0be0aaf1818560cdb45b872292100901f10b6509350d9f9ac285`  
		Last Modified: Wed, 06 Apr 2022 04:17:53 GMT  
		Size: 197.6 MB (197647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.2`

```console
$ docker pull sapmachine@sha256:fa3118e456ff81dddf9513a111384fc9955de6d9d35e158395bae1934f9092df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.2` - linux; amd64

```console
$ docker pull sapmachine@sha256:ace069bdddbd2ee49cfedda09056f8050f987394648b5a7394b9b0a47d86e49d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ed4b908a9544cc218e608a334742a506733f96b2e0e2793b53a9280e5062`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:31 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 06 Apr 2022 04:16:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbd16ff38383c60b8fc1bf647050936263de1dd59479348cbd39aa26485b59`  
		Last Modified: Wed, 06 Apr 2022 04:16:51 GMT  
		Size: 8.3 MB (8317679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7512af92b6ae0be0aaf1818560cdb45b872292100901f10b6509350d9f9ac285`  
		Last Modified: Wed, 06 Apr 2022 04:17:53 GMT  
		Size: 197.6 MB (197647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:18`

```console
$ docker pull sapmachine@sha256:6d2f324c58846d23bd61c3d6a7d4a33268ea65ea818f9b3be54a326292296fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:18` - linux; amd64

```console
$ docker pull sapmachine@sha256:907eebdd3c427d798ffda246dc2a0bea79201841e59c6e1bad8ba5cb163db45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235170363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4abbe0d9631f44da6ba0d2702a5115726c135ad849b1cf1967343d9268b032d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:15:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Wed, 06 Apr 2022 04:15:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148e1e83af18d1b33d250a5a3357663bc911656dda2c3c27777510d2e14a7c80`  
		Last Modified: Wed, 06 Apr 2022 04:17:14 GMT  
		Size: 7.9 MB (7925554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0c506459d3f09d4ba1d38e5686eb18086f1f56272abbe58ad284d26c7da004`  
		Last Modified: Wed, 06 Apr 2022 04:17:28 GMT  
		Size: 198.7 MB (198678517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:6d2f324c58846d23bd61c3d6a7d4a33268ea65ea818f9b3be54a326292296fb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:907eebdd3c427d798ffda246dc2a0bea79201841e59c6e1bad8ba5cb163db45e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235170363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4abbe0d9631f44da6ba0d2702a5115726c135ad849b1cf1967343d9268b032d`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:15:23 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-18-jdk=18     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:15:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-18
# Wed, 06 Apr 2022 04:15:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148e1e83af18d1b33d250a5a3357663bc911656dda2c3c27777510d2e14a7c80`  
		Last Modified: Wed, 06 Apr 2022 04:17:14 GMT  
		Size: 7.9 MB (7925554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd0c506459d3f09d4ba1d38e5686eb18086f1f56272abbe58ad284d26c7da004`  
		Last Modified: Wed, 06 Apr 2022 04:17:28 GMT  
		Size: 198.7 MB (198678517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:fa3118e456ff81dddf9513a111384fc9955de6d9d35e158395bae1934f9092df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:ace069bdddbd2ee49cfedda09056f8050f987394648b5a7394b9b0a47d86e49d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6248ed4b908a9544cc218e608a334742a506733f96b2e0e2793b53a9280e5062`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 05 Apr 2022 22:20:50 GMT
ADD file:b83df51ab7caf8a4dc35f730f5a18a59403300c59eecae4cf5779cba0f6fda6e in / 
# Tue, 05 Apr 2022 22:20:51 GMT
CMD ["bash"]
# Wed, 06 Apr 2022 04:14:43 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:31 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Wed, 06 Apr 2022 04:16:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 06 Apr 2022 04:16:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e0b25ef516347a097d75f8aea6bc0f42a4e8e70b057e84d85098d51f96d458f9`  
		Last Modified: Tue, 05 Apr 2022 13:14:03 GMT  
		Size: 28.6 MB (28566292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dbd16ff38383c60b8fc1bf647050936263de1dd59479348cbd39aa26485b59`  
		Last Modified: Wed, 06 Apr 2022 04:16:51 GMT  
		Size: 8.3 MB (8317679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7512af92b6ae0be0aaf1818560cdb45b872292100901f10b6509350d9f9ac285`  
		Last Modified: Wed, 06 Apr 2022 04:17:53 GMT  
		Size: 197.6 MB (197647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
