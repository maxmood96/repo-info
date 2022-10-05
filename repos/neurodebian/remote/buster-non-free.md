## `neurodebian:buster-non-free`

```console
$ docker pull neurodebian@sha256:1b8e6b396dd099b61e36a2b19d6900f814d81510c418f42a1d5cebf15aefd42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `neurodebian:buster-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:a2e3e436f3774637fecc2d35630111123e5ae75ba23ba63e83d57401b729b454
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61247897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d329a9df499d0dc0b3386b4766c5be22661ce5105b8fcf90606746add3e6bfec`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:50 GMT
ADD file:1fb366429a5df94c7ba642735d6aa77e201f90e0843de03721a6ad19f80ee4e0 in / 
# Tue, 04 Oct 2022 23:26:50 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 04:37:45 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:37:47 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 04:37:47 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 04:37:51 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 04:37:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:b6d6a76ebdbe1e858fec4564af6c6c3fe9e9bf1c502c8c8a51afd0fcf3374d44`  
		Last Modified: Tue, 04 Oct 2022 23:31:15 GMT  
		Size: 50.4 MB (50441102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a98ad9d5bfe5c93cdc5dd566aa7c846123d6b674612d8c22ce6c4506a1c72d`  
		Last Modified: Wed, 05 Oct 2022 04:40:45 GMT  
		Size: 10.5 MB (10501516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:370a8bc5b640eb70d850ea36e9b51ae7b8fc76946e82ae1bb0642d47f0e0eb73`  
		Last Modified: Wed, 05 Oct 2022 04:40:44 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f286e51e987b82a169deb249e7d1398676dca1955e72e0976dc9302cfe8b7a`  
		Last Modified: Wed, 05 Oct 2022 04:40:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c0eb25a875218ed1b804497338449bbaeb2129f8647aec7695c8ef06e71cad`  
		Last Modified: Wed, 05 Oct 2022 04:40:44 GMT  
		Size: 302.9 KB (302910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534645635d433d322d0e0a9f9eb06a9ea23d56fd282b1576d7af7234e822cba0`  
		Last Modified: Wed, 05 Oct 2022 04:40:54 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; arm64 variant v8

```console
$ docker pull neurodebian@sha256:ae50d50c11c32068f7b0f868f8975041e8cc6381108233aa6926e8f2b4dbb863
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59637153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1ca9d0cf271394b943e6c4dbc574cc3b61dbe9eed4fa82dbd4e4feaf92085c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:54 GMT
ADD file:ef2ee78fb3eda698ebec33ff4b6dea672e03908b0f8630a28acb33ec9a7c3e13 in / 
# Tue, 04 Oct 2022 23:44:55 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 03:58:26 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:58:28 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 03:58:29 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 03:58:33 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 03:58:40 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:504dcdd9b4a0035dba7a55a5312cf594c3d22fb99b7bf676d397c464db919009`  
		Last Modified: Tue, 04 Oct 2022 23:50:47 GMT  
		Size: 49.2 MB (49228885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d154496b8ab72771340bbbfcb90129abefba06a0df134e694e436c32723ecf`  
		Last Modified: Wed, 05 Oct 2022 04:02:31 GMT  
		Size: 10.3 MB (10297436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef89a9a6d8113e10f9e579ee92783e306a5fa8bfe2acfa01e2d78d7fd818107f`  
		Last Modified: Wed, 05 Oct 2022 04:02:29 GMT  
		Size: 1.7 KB (1741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23704a18d02fdbc4131c6f7adfaaec3730093c5504d02a143c4a78f637028721`  
		Last Modified: Wed, 05 Oct 2022 04:02:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d322400769bb470d58b21b11c9f6e84fb73d5e8603c40127b4804943ec7f7ec2`  
		Last Modified: Wed, 05 Oct 2022 04:02:30 GMT  
		Size: 108.5 KB (108492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ebd81db9bac845b1da95a5029d74042c0045701de4248a1c4a035311b28efe`  
		Last Modified: Wed, 05 Oct 2022 04:02:41 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `neurodebian:buster-non-free` - linux; 386

```console
$ docker pull neurodebian@sha256:fa77adad3506f7d86dae7b6965fe84a271c03357bb0d6a0a88cfcf84d9c5aec1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61982810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d524cf15f421c47fa01d99d0e92e1d401e54ffefa9ea0aec36d56ddd527a0e09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:39:52 GMT
ADD file:887aa5460e148ba204780ebe976e5627d5f4d0a07faf22b86afe146998d75d79 in / 
# Tue, 04 Oct 2022 23:39:53 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:14:43 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:14:44 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver keyserver.ubuntu.com --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Wed, 05 Oct 2022 02:14:45 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian buster main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel buster main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Wed, 05 Oct 2022 02:14:50 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:14:56 GMT
RUN [ -e /etc/apt/sources.list.d/debian.sources ] && srcs=/etc/apt/sources.list.d/debian.sources || srcs=/etc/apt/sources.list; sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list $srcs
```

-	Layers:
	-	`sha256:98d78922e3457a6697f2cdbddaab27dbb47e2e0beedb1a4348c56102c850b343`  
		Last Modified: Tue, 04 Oct 2022 23:45:58 GMT  
		Size: 51.2 MB (51202841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53a1c4ae5a735b6da355e52d679127188fc0385520109eb7c93e31b0fd3a7c5`  
		Last Modified: Wed, 05 Oct 2022 02:17:01 GMT  
		Size: 10.7 MB (10669155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127af1b441210177fdedbe41dc0aaf6ca644be580c15ae7a5cae51e8ff1bffce`  
		Last Modified: Wed, 05 Oct 2022 02:16:59 GMT  
		Size: 1.7 KB (1745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8999f6b03a0580644ff4a8ada4dec6b0d39eec0f624022a1b96f832f8fd28a21`  
		Last Modified: Wed, 05 Oct 2022 02:16:59 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5c07173b4dcb13dbcc2b4c04cdbb7546fb67e2b14f21eea7653356ac3845ba`  
		Last Modified: Wed, 05 Oct 2022 02:16:59 GMT  
		Size: 108.5 KB (108467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0b36a65a1c2c95edc9bf80ee22743a8f9009433ee1c689bb97051f7899e85`  
		Last Modified: Wed, 05 Oct 2022 02:17:11 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
