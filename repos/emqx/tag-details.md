<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.3`](#emqx43)
-	[`emqx:4.3.22`](#emqx4322)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.11`](#emqx4411)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.13`](#emqx5013)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:8d81cba337dfeaa1b2310fe6b6b55f5a79e7a22014d77ab9691937aebbd3b68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:e0dfb2c6239fb7f82b45b0a39361681184973ac74ff435873508cb028f4f4487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127221355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f6d4781d34568377a8af3b015cde0923bf669daeb5156c345c0a8ad44a1c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:56 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 03:48:56 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 03:49:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:49:07 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:49:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:08 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d3e57ec5f70305a1554472a8bc80d1caf9263b899fdc9e84d30606e2e849d5`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 2.6 MB (2569545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a38636ad2908276c756cc19c9eaf03c065b5766e78d0a3cf1ccbe466110f1`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46617899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4acfc8f57effa272b4a30ae405ece9fce1d7cdd766f45f3d96dad00dd8447`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46635832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59b8e6f00f0d3561339728542030d702d34a55f13d7e5a32a473eb6ed10271`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7dd73709b94fa0ef33a02bf7a0218d323d3ed9d16638aa6ace75784c30c8357c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111417879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b813fe567331d7d68c23ca54201ff7de9b2a7c0faf40a4e409cb6ed3ee0a45f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:35 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 21 Dec 2022 02:37:35 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 21 Dec 2022 02:37:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 21 Dec 2022 02:37:42 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 21 Dec 2022 02:37:42 GMT
WORKDIR /opt/emqx
# Wed, 21 Dec 2022 02:37:42 GMT
USER emqx
# Wed, 21 Dec 2022 02:37:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 21 Dec 2022 02:37:43 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 21 Dec 2022 02:37:43 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 21 Dec 2022 02:37:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:37:43 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f54b227d051db3a5adf4052f23f9f04079b36c5ee7325bc0bb89de5a0c01431`  
		Last Modified: Wed, 21 Dec 2022 02:38:23 GMT  
		Size: 2.6 MB (2559277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6294bd6555bd8ecb18f540f500f4c59148623e99e95097727bf3f066d0e5e7`  
		Last Modified: Wed, 21 Dec 2022 02:38:26 GMT  
		Size: 39.4 MB (39403616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28334a224641a108af0414ab663b2c97afdb9b7d3ca87b7e628b50444deef003`  
		Last Modified: Wed, 21 Dec 2022 02:38:26 GMT  
		Size: 39.4 MB (39409106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd76f1db199d5827e580d508673f871505dcd0788aae5af91b3138f18700dc5`  
		Last Modified: Wed, 21 Dec 2022 02:38:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3`

```console
$ docker pull emqx@sha256:477064c17ade339dffd72cb29d43d03d1a4bf8f2db8751f8ecc4291057a56274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3` - linux; amd64

```console
$ docker pull emqx@sha256:776c7ebd1ad82b0fdb4fb964c7893efc4db5d6dea6fd123c6f0768acf3d3b8dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dddd3a138ab5db23c6729e00989aa22437b88911d6b81aa403c58657dced7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:37 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:38 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 11 Jan 2023 03:48:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:48:47 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
USER emqx
# Wed, 11 Jan 2023 03:48:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:48:48 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:48:48 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 11 Jan 2023 03:48:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:48:48 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661145169f684ea6623410a6b2e6bac4fff75dcec9474b51911e88a29706557f`  
		Last Modified: Wed, 11 Jan 2023 03:49:39 GMT  
		Size: 4.6 MB (4612517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebf05a3530c36d245bf6c7e46809202091a05a222150006a341b1a10186a3b2`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee3e26cd384fe26b2d8d4d2e7bd81e7d5510d04394408e3716a9ad3f52cedb3`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b98ad0a8ea4aaf82a5a3a86a56e2d00279b789ed0568c21c210686fdc248f`  
		Last Modified: Wed, 11 Jan 2023 03:49:38 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9803d13f2887e3f9e287ab35fe5d3bf83f5a7404baf0ace6157c6409bb46ca0d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102846198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7717370b6f52a08cfa7b77daa9075c62a16e4d93fae6baa119fd6dde41882`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:19 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 21 Dec 2022 02:37:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 21 Dec 2022 02:37:27 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 21 Dec 2022 02:37:28 GMT
WORKDIR /opt/emqx
# Wed, 21 Dec 2022 02:37:28 GMT
USER emqx
# Wed, 21 Dec 2022 02:37:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 21 Dec 2022 02:37:28 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 21 Dec 2022 02:37:28 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 21 Dec 2022 02:37:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:37:28 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd6c73c4f5079d9f33c5b9fd8a0070a9ac92fa0e44194ab2c9a2e58ba5e661b`  
		Last Modified: Wed, 21 Dec 2022 02:38:11 GMT  
		Size: 4.5 MB (4490402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70d99423f90fb9b757a52e857f7feb92cb724c5dd4d4fbe83a2431772a449f`  
		Last Modified: Wed, 21 Dec 2022 02:38:14 GMT  
		Size: 36.2 MB (36216040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad5dd0deaa2677941018aaed289fa57c7106cb0bd14a4cf665fd8ec0314f18`  
		Last Modified: Wed, 21 Dec 2022 02:38:14 GMT  
		Size: 36.2 MB (36223809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b046a5dab4938961f37eabebcd6f35c6180a2bff6280a6cb11275120f588e5a5`  
		Last Modified: Wed, 21 Dec 2022 02:38:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.3.22`

```console
$ docker pull emqx@sha256:477064c17ade339dffd72cb29d43d03d1a4bf8f2db8751f8ecc4291057a56274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.3.22` - linux; amd64

```console
$ docker pull emqx@sha256:776c7ebd1ad82b0fdb4fb964c7893efc4db5d6dea6fd123c6f0768acf3d3b8dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104828515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7dddd3a138ab5db23c6729e00989aa22437b88911d6b81aa403c58657dced7`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:35:07 GMT
ADD file:67ceb946e54c26c505b5f9f393d77befbd5e9b3b5c069ca301e314ecc74456b0 in / 
# Wed, 11 Jan 2023 02:35:07 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:37 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:38 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 11 Jan 2023 03:48:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:48:47 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:48:48 GMT
USER emqx
# Wed, 11 Jan 2023 03:48:48 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:48:48 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:48:48 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 11 Jan 2023 03:48:48 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:48:48 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:548fcab5fe888f589dd092c68b813bfd65359878bd1950d6b753f749e82ebd7c`  
		Last Modified: Wed, 11 Jan 2023 02:39:48 GMT  
		Size: 27.1 MB (27140352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661145169f684ea6623410a6b2e6bac4fff75dcec9474b51911e88a29706557f`  
		Last Modified: Wed, 11 Jan 2023 03:49:39 GMT  
		Size: 4.6 MB (4612517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ebf05a3530c36d245bf6c7e46809202091a05a222150006a341b1a10186a3b2`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee3e26cd384fe26b2d8d4d2e7bd81e7d5510d04394408e3716a9ad3f52cedb3`  
		Last Modified: Wed, 11 Jan 2023 03:49:42 GMT  
		Size: 36.5 MB (36537374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d94b98ad0a8ea4aaf82a5a3a86a56e2d00279b789ed0568c21c210686fdc248f`  
		Last Modified: Wed, 11 Jan 2023 03:49:38 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.3.22` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:9803d13f2887e3f9e287ab35fe5d3bf83f5a7404baf0ace6157c6409bb46ca0d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102846198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a7717370b6f52a08cfa7b77daa9075c62a16e4d93fae6baa119fd6dde41882`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:19 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:19 GMT
ENV EMQX_VERSION=4.3.22
# Wed, 21 Dec 2022 02:37:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="e5f6874eb29f83cce9c84afae95cc05de11ed8aa47f046783afa1c75e812a4b7"; fi;     if [ ${arch} = "arm64" ]; then sha256="85bf586fdf1c11f4057f6137faa4390100a3f3eb0e285e8a68e63c7d15bea09b"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${ID}${VERSION_ID}-${EMQX_VERSION}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 21 Dec 2022 02:37:27 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 21 Dec 2022 02:37:28 GMT
WORKDIR /opt/emqx
# Wed, 21 Dec 2022 02:37:28 GMT
USER emqx
# Wed, 21 Dec 2022 02:37:28 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 21 Dec 2022 02:37:28 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 21 Dec 2022 02:37:28 GMT
COPY file:715d536465bb73dc7e7d11b7af4806884602823836c36e9ec561de98ccbf3424 in /usr/bin/ 
# Wed, 21 Dec 2022 02:37:28 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:37:28 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd6c73c4f5079d9f33c5b9fd8a0070a9ac92fa0e44194ab2c9a2e58ba5e661b`  
		Last Modified: Wed, 21 Dec 2022 02:38:11 GMT  
		Size: 4.5 MB (4490402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe70d99423f90fb9b757a52e857f7feb92cb724c5dd4d4fbe83a2431772a449f`  
		Last Modified: Wed, 21 Dec 2022 02:38:14 GMT  
		Size: 36.2 MB (36216040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ad5dd0deaa2677941018aaed289fa57c7106cb0bd14a4cf665fd8ec0314f18`  
		Last Modified: Wed, 21 Dec 2022 02:38:14 GMT  
		Size: 36.2 MB (36223809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b046a5dab4938961f37eabebcd6f35c6180a2bff6280a6cb11275120f588e5a5`  
		Last Modified: Wed, 21 Dec 2022 02:38:11 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:8d81cba337dfeaa1b2310fe6b6b55f5a79e7a22014d77ab9691937aebbd3b68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:e0dfb2c6239fb7f82b45b0a39361681184973ac74ff435873508cb028f4f4487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127221355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f6d4781d34568377a8af3b015cde0923bf669daeb5156c345c0a8ad44a1c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:56 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 03:48:56 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 03:49:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:49:07 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:49:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:08 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d3e57ec5f70305a1554472a8bc80d1caf9263b899fdc9e84d30606e2e849d5`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 2.6 MB (2569545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a38636ad2908276c756cc19c9eaf03c065b5766e78d0a3cf1ccbe466110f1`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46617899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4acfc8f57effa272b4a30ae405ece9fce1d7cdd766f45f3d96dad00dd8447`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46635832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59b8e6f00f0d3561339728542030d702d34a55f13d7e5a32a473eb6ed10271`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7dd73709b94fa0ef33a02bf7a0218d323d3ed9d16638aa6ace75784c30c8357c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111417879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b813fe567331d7d68c23ca54201ff7de9b2a7c0faf40a4e409cb6ed3ee0a45f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:35 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 21 Dec 2022 02:37:35 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 21 Dec 2022 02:37:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 21 Dec 2022 02:37:42 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 21 Dec 2022 02:37:42 GMT
WORKDIR /opt/emqx
# Wed, 21 Dec 2022 02:37:42 GMT
USER emqx
# Wed, 21 Dec 2022 02:37:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 21 Dec 2022 02:37:43 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 21 Dec 2022 02:37:43 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 21 Dec 2022 02:37:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:37:43 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f54b227d051db3a5adf4052f23f9f04079b36c5ee7325bc0bb89de5a0c01431`  
		Last Modified: Wed, 21 Dec 2022 02:38:23 GMT  
		Size: 2.6 MB (2559277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6294bd6555bd8ecb18f540f500f4c59148623e99e95097727bf3f066d0e5e7`  
		Last Modified: Wed, 21 Dec 2022 02:38:26 GMT  
		Size: 39.4 MB (39403616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28334a224641a108af0414ab663b2c97afdb9b7d3ca87b7e628b50444deef003`  
		Last Modified: Wed, 21 Dec 2022 02:38:26 GMT  
		Size: 39.4 MB (39409106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd76f1db199d5827e580d508673f871505dcd0788aae5af91b3138f18700dc5`  
		Last Modified: Wed, 21 Dec 2022 02:38:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.11`

```console
$ docker pull emqx@sha256:8d81cba337dfeaa1b2310fe6b6b55f5a79e7a22014d77ab9691937aebbd3b68a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.11` - linux; amd64

```console
$ docker pull emqx@sha256:e0dfb2c6239fb7f82b45b0a39361681184973ac74ff435873508cb028f4f4487
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.2 MB (127221355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f6d4781d34568377a8af3b015cde0923bf669daeb5156c345c0a8ad44a1c4`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:48:56 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:48:56 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 11 Jan 2023 03:48:56 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 11 Jan 2023 03:49:01 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 11 Jan 2023 03:49:07 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:07 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:08 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:08 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 11 Jan 2023 03:49:08 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:08 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:08 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d3e57ec5f70305a1554472a8bc80d1caf9263b899fdc9e84d30606e2e849d5`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 2.6 MB (2569545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6a38636ad2908276c756cc19c9eaf03c065b5766e78d0a3cf1ccbe466110f1`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46617899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff4acfc8f57effa272b4a30ae405ece9fce1d7cdd766f45f3d96dad00dd8447`  
		Last Modified: Wed, 11 Jan 2023 03:49:56 GMT  
		Size: 46.6 MB (46635832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59b8e6f00f0d3561339728542030d702d34a55f13d7e5a32a473eb6ed10271`  
		Last Modified: Wed, 11 Jan 2023 03:49:51 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.11` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7dd73709b94fa0ef33a02bf7a0218d323d3ed9d16638aa6ace75784c30c8357c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.4 MB (111417879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b813fe567331d7d68c23ca54201ff7de9b2a7c0faf40a4e409cb6ed3ee0a45f0`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:34 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:35 GMT
ENV EMQX_VERSION=4.4.11
# Wed, 21 Dec 2022 02:37:35 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 21 Dec 2022 02:37:38 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="652fb25a2a5c9d4e9fc029a4094d39c5bd824c78ad77361fb5fee09a940209a6"; fi;     if [ ${arch} = "arm64" ]; then sha256="6532a0f93fe8ce419633142b376107f3d7a2a79df24ce95551026b9e144a77b8"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 21 Dec 2022 02:37:42 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx
# Wed, 21 Dec 2022 02:37:42 GMT
WORKDIR /opt/emqx
# Wed, 21 Dec 2022 02:37:42 GMT
USER emqx
# Wed, 21 Dec 2022 02:37:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 21 Dec 2022 02:37:43 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 21 Dec 2022 02:37:43 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 21 Dec 2022 02:37:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 21 Dec 2022 02:37:43 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f54b227d051db3a5adf4052f23f9f04079b36c5ee7325bc0bb89de5a0c01431`  
		Last Modified: Wed, 21 Dec 2022 02:38:23 GMT  
		Size: 2.6 MB (2559277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6294bd6555bd8ecb18f540f500f4c59148623e99e95097727bf3f066d0e5e7`  
		Last Modified: Wed, 21 Dec 2022 02:38:26 GMT  
		Size: 39.4 MB (39403616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28334a224641a108af0414ab663b2c97afdb9b7d3ca87b7e628b50444deef003`  
		Last Modified: Wed, 21 Dec 2022 02:38:26 GMT  
		Size: 39.4 MB (39409106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd76f1db199d5827e580d508673f871505dcd0788aae5af91b3138f18700dc5`  
		Last Modified: Wed, 21 Dec 2022 02:38:22 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:d452f1d78c761be7eed83586823b460a7213929b1997a610af1da4d0e1cfe059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:125987045f6ce0032de67377df4526dfd98fd952f4cf7d6acf74c40cde2d5cbf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91182859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb848811cfcb263f6b942d143b5b29676b99cf6c3b5f507d547e69d5665cd08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 29 Dec 2022 16:47:27 GMT
ENV EMQX_VERSION=5.0.13
# Thu, 29 Dec 2022 16:47:28 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Thu, 29 Dec 2022 16:47:28 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Thu, 29 Dec 2022 16:47:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 29 Dec 2022 16:47:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 29 Dec 2022 16:47:33 GMT
WORKDIR /opt/emqx
# Thu, 29 Dec 2022 16:47:33 GMT
USER emqx
# Thu, 29 Dec 2022 16:47:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 29 Dec 2022 16:47:33 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 29 Dec 2022 16:47:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 29 Dec 2022 16:47:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 29 Dec 2022 16:47:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00bfb98ad2c7fcd02eb0e70fa6f4c91eeb687fc3062f5a249a46bd6e29124a8`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 3.0 MB (3002677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32322aa000b6d18c777989890f9d396f187818464d2d0eb2b436bddbffda647f`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c10bc5c21d8d6d12621e7d39ce31f1962f258ddcafa714ac13754b5a741476`  
		Last Modified: Thu, 29 Dec 2022 16:47:57 GMT  
		Size: 58.1 MB (58130393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd957cd7da661a6bf4d762dac3c8ad42c3a7467d98d94c5582e8476e652195a`  
		Last Modified: Thu, 29 Dec 2022 16:47:51 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:d452f1d78c761be7eed83586823b460a7213929b1997a610af1da4d0e1cfe059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:125987045f6ce0032de67377df4526dfd98fd952f4cf7d6acf74c40cde2d5cbf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91182859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb848811cfcb263f6b942d143b5b29676b99cf6c3b5f507d547e69d5665cd08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 29 Dec 2022 16:47:27 GMT
ENV EMQX_VERSION=5.0.13
# Thu, 29 Dec 2022 16:47:28 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Thu, 29 Dec 2022 16:47:28 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Thu, 29 Dec 2022 16:47:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 29 Dec 2022 16:47:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 29 Dec 2022 16:47:33 GMT
WORKDIR /opt/emqx
# Thu, 29 Dec 2022 16:47:33 GMT
USER emqx
# Thu, 29 Dec 2022 16:47:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 29 Dec 2022 16:47:33 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 29 Dec 2022 16:47:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 29 Dec 2022 16:47:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 29 Dec 2022 16:47:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00bfb98ad2c7fcd02eb0e70fa6f4c91eeb687fc3062f5a249a46bd6e29124a8`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 3.0 MB (3002677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32322aa000b6d18c777989890f9d396f187818464d2d0eb2b436bddbffda647f`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c10bc5c21d8d6d12621e7d39ce31f1962f258ddcafa714ac13754b5a741476`  
		Last Modified: Thu, 29 Dec 2022 16:47:57 GMT  
		Size: 58.1 MB (58130393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd957cd7da661a6bf4d762dac3c8ad42c3a7467d98d94c5582e8476e652195a`  
		Last Modified: Thu, 29 Dec 2022 16:47:51 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.13`

```console
$ docker pull emqx@sha256:d452f1d78c761be7eed83586823b460a7213929b1997a610af1da4d0e1cfe059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.13` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.13` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:125987045f6ce0032de67377df4526dfd98fd952f4cf7d6acf74c40cde2d5cbf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91182859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb848811cfcb263f6b942d143b5b29676b99cf6c3b5f507d547e69d5665cd08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 29 Dec 2022 16:47:27 GMT
ENV EMQX_VERSION=5.0.13
# Thu, 29 Dec 2022 16:47:28 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Thu, 29 Dec 2022 16:47:28 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Thu, 29 Dec 2022 16:47:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 29 Dec 2022 16:47:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 29 Dec 2022 16:47:33 GMT
WORKDIR /opt/emqx
# Thu, 29 Dec 2022 16:47:33 GMT
USER emqx
# Thu, 29 Dec 2022 16:47:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 29 Dec 2022 16:47:33 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 29 Dec 2022 16:47:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 29 Dec 2022 16:47:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 29 Dec 2022 16:47:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00bfb98ad2c7fcd02eb0e70fa6f4c91eeb687fc3062f5a249a46bd6e29124a8`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 3.0 MB (3002677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32322aa000b6d18c777989890f9d396f187818464d2d0eb2b436bddbffda647f`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c10bc5c21d8d6d12621e7d39ce31f1962f258ddcafa714ac13754b5a741476`  
		Last Modified: Thu, 29 Dec 2022 16:47:57 GMT  
		Size: 58.1 MB (58130393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd957cd7da661a6bf4d762dac3c8ad42c3a7467d98d94c5582e8476e652195a`  
		Last Modified: Thu, 29 Dec 2022 16:47:51 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:d452f1d78c761be7eed83586823b460a7213929b1997a610af1da4d0e1cfe059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:00e325eeaf332d45588fecb0bbfed8ce232d07e8b789da22d46eec4183f10ac3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100088224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be156fa8346c02b9558c66eff46e1d2dc0c29d698672163852705a7d846b43e`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 11 Jan 2023 02:34:44 GMT
ADD file:e2398d0bf516084b2b37ba1bb76b86d56e66999831df692461679fbd6a5d8eb6 in / 
# Wed, 11 Jan 2023 02:34:44 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 03:49:16 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 03:49:16 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 11 Jan 2023 03:49:16 GMT
ENV EMQX_VERSION=5.0.13
# Wed, 11 Jan 2023 03:49:16 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Wed, 11 Jan 2023 03:49:17 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Wed, 11 Jan 2023 03:49:17 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 11 Jan 2023 03:49:23 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 11 Jan 2023 03:49:24 GMT
WORKDIR /opt/emqx
# Wed, 11 Jan 2023 03:49:24 GMT
USER emqx
# Wed, 11 Jan 2023 03:49:24 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 11 Jan 2023 03:49:24 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 11 Jan 2023 03:49:24 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 11 Jan 2023 03:49:24 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 11 Jan 2023 03:49:24 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:8740c948ffd4c816ea7ca963f99ca52f4788baa23f228da9581a9ea2edd3fcd7`  
		Last Modified: Wed, 11 Jan 2023 02:39:07 GMT  
		Size: 31.4 MB (31396972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1226f5729eeebf1d9e397edf672aef9dc2809741454ab2d1a2f58a4bb3f67eb0`  
		Last Modified: Wed, 11 Jan 2023 03:50:07 GMT  
		Size: 3.0 MB (2987690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a786684ff862ef4f11abc26cfb08583cf925746ea80d7c34769aa93aa99660e7`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbce4d1d57f5821c0f730ea811bd7b669a1c31d95e617e0278224a14b765719`  
		Last Modified: Wed, 11 Jan 2023 03:50:14 GMT  
		Size: 65.7 MB (65698554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48bb659c4715b75d19566fe97d471ce0b1c22783930b49dd3f44e47b0d4f862`  
		Last Modified: Wed, 11 Jan 2023 03:50:06 GMT  
		Size: 902.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:125987045f6ce0032de67377df4526dfd98fd952f4cf7d6acf74c40cde2d5cbf
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91182859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb848811cfcb263f6b942d143b5b29676b99cf6c3b5f507d547e69d5665cd08`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:48 GMT
ADD file:3ff0cc8d111595978eb50cdba91144382ce083c400d45785d53dbb03615a4890 in / 
# Wed, 21 Dec 2022 01:39:48 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:37:51 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:37:51 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Thu, 29 Dec 2022 16:47:27 GMT
ENV EMQX_VERSION=5.0.13
# Thu, 29 Dec 2022 16:47:28 GMT
ENV AMD64_SHA256=d52ea9a5c07cb31106f3bb7ac541a269ce205a6d1c9d847d7fe01ad39da0b1a4
# Thu, 29 Dec 2022 16:47:28 GMT
ENV ARM64_SHA256=5f02e38b6fbd07c23455890a59b041f8d91fcceeeaedaec090435f913927538e
# Thu, 29 Dec 2022 16:47:28 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Thu, 29 Dec 2022 16:47:32 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Thu, 29 Dec 2022 16:47:33 GMT
WORKDIR /opt/emqx
# Thu, 29 Dec 2022 16:47:33 GMT
USER emqx
# Thu, 29 Dec 2022 16:47:33 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Thu, 29 Dec 2022 16:47:33 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Thu, 29 Dec 2022 16:47:33 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Thu, 29 Dec 2022 16:47:33 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Thu, 29 Dec 2022 16:47:33 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:4b7f5b2a311310809ab89d92f6f71b0462722fe855d3b92c93098a528aa08791`  
		Last Modified: Wed, 21 Dec 2022 01:43:12 GMT  
		Size: 30.0 MB (30044772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00bfb98ad2c7fcd02eb0e70fa6f4c91eeb687fc3062f5a249a46bd6e29124a8`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 3.0 MB (3002677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32322aa000b6d18c777989890f9d396f187818464d2d0eb2b436bddbffda647f`  
		Last Modified: Wed, 21 Dec 2022 02:38:37 GMT  
		Size: 4.1 KB (4114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c10bc5c21d8d6d12621e7d39ce31f1962f258ddcafa714ac13754b5a741476`  
		Last Modified: Thu, 29 Dec 2022 16:47:57 GMT  
		Size: 58.1 MB (58130393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd957cd7da661a6bf4d762dac3c8ad42c3a7467d98d94c5582e8476e652195a`  
		Last Modified: Thu, 29 Dec 2022 16:47:51 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
