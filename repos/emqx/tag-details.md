<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `emqx`

-	[`emqx:4`](#emqx4)
-	[`emqx:4.4`](#emqx44)
-	[`emqx:4.4.18`](#emqx4418)
-	[`emqx:5`](#emqx5)
-	[`emqx:5.0`](#emqx50)
-	[`emqx:5.0.24`](#emqx5024)
-	[`emqx:latest`](#emqxlatest)

## `emqx:4`

```console
$ docker pull emqx@sha256:ba6458c1e52712021388a843656eb312979b91d5abb21becde3f838d5f5c07b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4` - linux; amd64

```console
$ docker pull emqx@sha256:ddd36e7bde6ee03eab04572f1eee4895fe599a1329cc371d680a8dec6c190fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81276585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b743eaf2ae221d8564f61fdf640bd469496af19f93a5d02b365159c6cdbb008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 20:41:21 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 20:41:21 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 20:41:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 20:41:26 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:26 GMT
USER emqx
# Wed, 03 May 2023 20:41:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:26 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 20:41:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 20:41:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8eb785168b6c6935f1c60a43366b1ff3387cc04c558257bd79cc16f0333733`  
		Last Modified: Wed, 03 May 2023 20:41:53 GMT  
		Size: 2.6 MB (2569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a6e85cba209db12bd844ffd163b7c5c79adbd21e67e21298f38dbfc22840c`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63510ee4876f5d6b05df3702d30b85a41e257cb918695580226753ba63c9`  
		Last Modified: Wed, 03 May 2023 20:41:57 GMT  
		Size: 47.3 MB (47298226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d549e1393d2fd2d0b85822c9213eb06d7b4781b69e3e39a1b2b96466f2fb59`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7688768a72b7fa9010de1fe1700217548815af988a17de2b9bd65a60a454e067
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa151f551c374dd3d4e17e89a56c17041e9bfb540a498c24aa000dd2426bd8d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:31 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:32 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 23 May 2023 01:42:32 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 23 May 2023 01:42:32 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 23 May 2023 01:42:36 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 May 2023 01:42:36 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:36 GMT
USER emqx
# Tue, 23 May 2023 01:42:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 May 2023 01:42:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 May 2023 01:42:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e3be4db2d4e51135129c236fbac8797820630823c20cc285003c52204383a9`  
		Last Modified: Tue, 23 May 2023 01:42:59 GMT  
		Size: 2.6 MB (2559465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea7a7747eda949c0b01b8782f9bce294e4d252d81ad86e697b761fa378ee86`  
		Last Modified: Tue, 23 May 2023 01:42:58 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762dea4f4f570daf68e5a15a784874befa9af9aade89f064f7aa6c95956eb8af`  
		Last Modified: Tue, 23 May 2023 01:43:02 GMT  
		Size: 40.1 MB (40079880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a354585a72ccdf88f7dbe22e0f7173467f9273217904a5f411184836f4b2487d`  
		Last Modified: Tue, 23 May 2023 01:42:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4`

```console
$ docker pull emqx@sha256:ba6458c1e52712021388a843656eb312979b91d5abb21becde3f838d5f5c07b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4` - linux; amd64

```console
$ docker pull emqx@sha256:ddd36e7bde6ee03eab04572f1eee4895fe599a1329cc371d680a8dec6c190fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81276585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b743eaf2ae221d8564f61fdf640bd469496af19f93a5d02b365159c6cdbb008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 20:41:21 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 20:41:21 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 20:41:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 20:41:26 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:26 GMT
USER emqx
# Wed, 03 May 2023 20:41:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:26 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 20:41:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 20:41:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8eb785168b6c6935f1c60a43366b1ff3387cc04c558257bd79cc16f0333733`  
		Last Modified: Wed, 03 May 2023 20:41:53 GMT  
		Size: 2.6 MB (2569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a6e85cba209db12bd844ffd163b7c5c79adbd21e67e21298f38dbfc22840c`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63510ee4876f5d6b05df3702d30b85a41e257cb918695580226753ba63c9`  
		Last Modified: Wed, 03 May 2023 20:41:57 GMT  
		Size: 47.3 MB (47298226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d549e1393d2fd2d0b85822c9213eb06d7b4781b69e3e39a1b2b96466f2fb59`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7688768a72b7fa9010de1fe1700217548815af988a17de2b9bd65a60a454e067
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa151f551c374dd3d4e17e89a56c17041e9bfb540a498c24aa000dd2426bd8d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:31 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:32 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 23 May 2023 01:42:32 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 23 May 2023 01:42:32 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 23 May 2023 01:42:36 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 May 2023 01:42:36 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:36 GMT
USER emqx
# Tue, 23 May 2023 01:42:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 May 2023 01:42:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 May 2023 01:42:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e3be4db2d4e51135129c236fbac8797820630823c20cc285003c52204383a9`  
		Last Modified: Tue, 23 May 2023 01:42:59 GMT  
		Size: 2.6 MB (2559465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea7a7747eda949c0b01b8782f9bce294e4d252d81ad86e697b761fa378ee86`  
		Last Modified: Tue, 23 May 2023 01:42:58 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762dea4f4f570daf68e5a15a784874befa9af9aade89f064f7aa6c95956eb8af`  
		Last Modified: Tue, 23 May 2023 01:43:02 GMT  
		Size: 40.1 MB (40079880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a354585a72ccdf88f7dbe22e0f7173467f9273217904a5f411184836f4b2487d`  
		Last Modified: Tue, 23 May 2023 01:42:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:4.4.18`

```console
$ docker pull emqx@sha256:ba6458c1e52712021388a843656eb312979b91d5abb21becde3f838d5f5c07b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:4.4.18` - linux; amd64

```console
$ docker pull emqx@sha256:ddd36e7bde6ee03eab04572f1eee4895fe599a1329cc371d680a8dec6c190fa6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81276585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b743eaf2ae221d8564f61fdf640bd469496af19f93a5d02b365159c6cdbb008`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:21 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Wed, 03 May 2023 20:41:21 GMT
ENV EMQX_VERSION=4.4.18
# Wed, 03 May 2023 20:41:21 GMT
ENV OTP=otp24.3.4.2-1
# Wed, 03 May 2023 20:41:26 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Wed, 03 May 2023 20:41:26 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:26 GMT
USER emqx
# Wed, 03 May 2023 20:41:26 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:26 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Wed, 03 May 2023 20:41:26 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Wed, 03 May 2023 20:41:26 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:27 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8eb785168b6c6935f1c60a43366b1ff3387cc04c558257bd79cc16f0333733`  
		Last Modified: Wed, 03 May 2023 20:41:53 GMT  
		Size: 2.6 MB (2569624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67a6e85cba209db12bd844ffd163b7c5c79adbd21e67e21298f38dbfc22840c`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 4.1 KB (4111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ffa63510ee4876f5d6b05df3702d30b85a41e257cb918695580226753ba63c9`  
		Last Modified: Wed, 03 May 2023 20:41:57 GMT  
		Size: 47.3 MB (47298226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d549e1393d2fd2d0b85822c9213eb06d7b4781b69e3e39a1b2b96466f2fb59`  
		Last Modified: Wed, 03 May 2023 20:41:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:4.4.18` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:7688768a72b7fa9010de1fe1700217548815af988a17de2b9bd65a60a454e067
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72697315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa151f551c374dd3d4e17e89a56c17041e9bfb540a498c24aa000dd2426bd8d`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:31 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl unzip ca-certificates;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:32 GMT
RUN set -eu;     groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx
# Tue, 23 May 2023 01:42:32 GMT
ENV EMQX_VERSION=4.4.18
# Tue, 23 May 2023 01:42:32 GMT
ENV OTP=otp24.3.4.2-1
# Tue, 23 May 2023 01:42:36 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="53712834a3cf209e488b97842ed9d6bae887e6e79ebaae3a0887018aab59b05b"; fi;     if [ ${arch} = "arm64" ]; then sha256="5fe04b2a10fc5e43ee582b38ecd526480a44ae277f5e6aa68ccd85f45e76baad"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${OTP}-${ID}${VERSION_ID}-${arch}.zip";     curl -f -O -L https://www.emqx.com/en/downloads/broker/${EMQX_VERSION}/${pkg};     echo "$sha256 *$pkg" | sha256sum -c || exit 1;     unzip -q -d /opt $pkg;     chgrp -Rf emqx /opt/emqx;     chmod -Rf g+w /opt/emqx;     chown -Rf emqx /opt/emqx;     ln -s /opt/emqx/bin/* /usr/local/bin/;     rm -rf $pkg
# Tue, 23 May 2023 01:42:36 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:36 GMT
USER emqx
# Tue, 23 May 2023 01:42:36 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:36 GMT
EXPOSE 11883 18083 1883 4369 4370 5369 6369 6370 8081 8083 8084 8883
# Tue, 23 May 2023 01:42:36 GMT
COPY file:6dd7e4492be7572c69a0409bd663714c620b2048d81308e1877901073db7f426 in /usr/bin/ 
# Tue, 23 May 2023 01:42:36 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:36 GMT
CMD ["emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e3be4db2d4e51135129c236fbac8797820630823c20cc285003c52204383a9`  
		Last Modified: Tue, 23 May 2023 01:42:59 GMT  
		Size: 2.6 MB (2559465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fea7a7747eda949c0b01b8782f9bce294e4d252d81ad86e697b761fa378ee86`  
		Last Modified: Tue, 23 May 2023 01:42:58 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762dea4f4f570daf68e5a15a784874befa9af9aade89f064f7aa6c95956eb8af`  
		Last Modified: Tue, 23 May 2023 01:43:02 GMT  
		Size: 40.1 MB (40079880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a354585a72ccdf88f7dbe22e0f7173467f9273217904a5f411184836f4b2487d`  
		Last Modified: Tue, 23 May 2023 01:42:59 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5`

```console
$ docker pull emqx@sha256:655d3f9b06d330cd3e50e4a97eadc2b1ff1e56f8e414ade3f85047b92a61ab2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e814162a881a076c095cd9780167b8742a18bd46afd2ecc0e3f0c019f194549
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a249e8111403d80b28441f004ac7b3b9a576fcbe337c24b09595e9c3993d50`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:43 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 23 May 2023 01:42:43 GMT
ENV EMQX_VERSION=5.0.24
# Tue, 23 May 2023 01:42:43 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Tue, 23 May 2023 01:42:43 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Tue, 23 May 2023 01:42:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 23 May 2023 01:42:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 23 May 2023 01:42:49 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:49 GMT
USER emqx
# Tue, 23 May 2023 01:42:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 23 May 2023 01:42:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 23 May 2023 01:42:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345ceedc06f3b0ae12a8eb9f0f0e7dd52b3ae9800880811d86f7c26b0651446`  
		Last Modified: Tue, 23 May 2023 01:43:12 GMT  
		Size: 3.0 MB (3002990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b78e6c4890d65e6f6f17dbd7faa9d396eaad9d65dd2bbeb2e49aee524b18b1e`  
		Last Modified: Tue, 23 May 2023 01:43:11 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3928ab53fc1ed36f55e43718a8e82fdc4b572ff52ec108e1cc737d144d1f63`  
		Last Modified: Tue, 23 May 2023 01:43:18 GMT  
		Size: 68.4 MB (68360170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629c5a6040608e24f6cca4a4a2dd9e31e4baa54d425e39557dc3c38d6204758`  
		Last Modified: Tue, 23 May 2023 01:43:15 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0`

```console
$ docker pull emqx@sha256:655d3f9b06d330cd3e50e4a97eadc2b1ff1e56f8e414ade3f85047b92a61ab2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e814162a881a076c095cd9780167b8742a18bd46afd2ecc0e3f0c019f194549
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a249e8111403d80b28441f004ac7b3b9a576fcbe337c24b09595e9c3993d50`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:43 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 23 May 2023 01:42:43 GMT
ENV EMQX_VERSION=5.0.24
# Tue, 23 May 2023 01:42:43 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Tue, 23 May 2023 01:42:43 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Tue, 23 May 2023 01:42:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 23 May 2023 01:42:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 23 May 2023 01:42:49 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:49 GMT
USER emqx
# Tue, 23 May 2023 01:42:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 23 May 2023 01:42:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 23 May 2023 01:42:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345ceedc06f3b0ae12a8eb9f0f0e7dd52b3ae9800880811d86f7c26b0651446`  
		Last Modified: Tue, 23 May 2023 01:43:12 GMT  
		Size: 3.0 MB (3002990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b78e6c4890d65e6f6f17dbd7faa9d396eaad9d65dd2bbeb2e49aee524b18b1e`  
		Last Modified: Tue, 23 May 2023 01:43:11 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3928ab53fc1ed36f55e43718a8e82fdc4b572ff52ec108e1cc737d144d1f63`  
		Last Modified: Tue, 23 May 2023 01:43:18 GMT  
		Size: 68.4 MB (68360170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629c5a6040608e24f6cca4a4a2dd9e31e4baa54d425e39557dc3c38d6204758`  
		Last Modified: Tue, 23 May 2023 01:43:15 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:5.0.24`

```console
$ docker pull emqx@sha256:655d3f9b06d330cd3e50e4a97eadc2b1ff1e56f8e414ade3f85047b92a61ab2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:5.0.24` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:5.0.24` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e814162a881a076c095cd9780167b8742a18bd46afd2ecc0e3f0c019f194549
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a249e8111403d80b28441f004ac7b3b9a576fcbe337c24b09595e9c3993d50`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:43 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 23 May 2023 01:42:43 GMT
ENV EMQX_VERSION=5.0.24
# Tue, 23 May 2023 01:42:43 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Tue, 23 May 2023 01:42:43 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Tue, 23 May 2023 01:42:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 23 May 2023 01:42:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 23 May 2023 01:42:49 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:49 GMT
USER emqx
# Tue, 23 May 2023 01:42:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 23 May 2023 01:42:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 23 May 2023 01:42:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345ceedc06f3b0ae12a8eb9f0f0e7dd52b3ae9800880811d86f7c26b0651446`  
		Last Modified: Tue, 23 May 2023 01:43:12 GMT  
		Size: 3.0 MB (3002990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b78e6c4890d65e6f6f17dbd7faa9d396eaad9d65dd2bbeb2e49aee524b18b1e`  
		Last Modified: Tue, 23 May 2023 01:43:11 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3928ab53fc1ed36f55e43718a8e82fdc4b572ff52ec108e1cc737d144d1f63`  
		Last Modified: Tue, 23 May 2023 01:43:18 GMT  
		Size: 68.4 MB (68360170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629c5a6040608e24f6cca4a4a2dd9e31e4baa54d425e39557dc3c38d6204758`  
		Last Modified: Tue, 23 May 2023 01:43:15 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `emqx:latest`

```console
$ docker pull emqx@sha256:655d3f9b06d330cd3e50e4a97eadc2b1ff1e56f8e414ade3f85047b92a61ab2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `emqx:latest` - linux; amd64

```console
$ docker pull emqx@sha256:a931690452e02b93a0625abe8d483b1e9923a4e2cc982bd847d556a6215c0291
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.3 MB (110336527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e172d0aa2301d30ab91b050589e47314a8390226a6653bdaf36841b2df397f1`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 02 May 2023 23:46:59 GMT
ADD file:a2378c1b12e95db69e24b9d347441678c6f23239292cce3c822b1524992b6ec4 in / 
# Tue, 02 May 2023 23:47:00 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:41:35 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 20:41:35 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Wed, 03 May 2023 20:41:35 GMT
ENV EMQX_VERSION=5.0.24
# Wed, 03 May 2023 20:41:35 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Wed, 03 May 2023 20:41:35 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Wed, 03 May 2023 20:41:35 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Wed, 03 May 2023 20:41:42 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Wed, 03 May 2023 20:41:42 GMT
WORKDIR /opt/emqx
# Wed, 03 May 2023 20:41:42 GMT
USER emqx
# Wed, 03 May 2023 20:41:42 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Wed, 03 May 2023 20:41:42 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Wed, 03 May 2023 20:41:43 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Wed, 03 May 2023 20:41:43 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Wed, 03 May 2023 20:41:43 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:9e3ea8720c6de96cc9ad544dddc695a3ab73f5581c5d954e0504cc4f80fb5e5c`  
		Last Modified: Tue, 02 May 2023 23:50:22 GMT  
		Size: 31.4 MB (31403516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5957f4c2c59058c37f59efc3852d835fcde06615f63c5cfef45d730217c636bc`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 3.0 MB (2987809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41c71048f2095a50b4a59192eed9adf44fc00ca48e913017a9431eabc732636`  
		Last Modified: Wed, 03 May 2023 20:42:07 GMT  
		Size: 4.1 KB (4106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f37bfff742120de1049760c5919c61e746dd4cbf52976ff0a1326eed4fee0b71`  
		Last Modified: Wed, 03 May 2023 20:42:15 GMT  
		Size: 75.9 MB (75940193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0707a5d53d9067042f376318258bce6018f19d5c27176e8d4fc0a03a70d7680`  
		Last Modified: Wed, 03 May 2023 20:42:06 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `emqx:latest` - linux; arm64 variant v8

```console
$ docker pull emqx@sha256:6e814162a881a076c095cd9780167b8742a18bd46afd2ecc0e3f0c019f194549
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.4 MB (101420925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a249e8111403d80b28441f004ac7b3b9a576fcbe337c24b09595e9c3993d50`
-	Entrypoint: `["\/usr\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["\/opt\/emqx\/bin\/emqx","foreground"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:42:42 GMT
RUN set -eu;     apt-get update;     apt-get install -y --no-install-recommends curl ca-certificates procps;     rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:42:43 GMT
RUN groupadd -r -g 1000 emqx;     useradd -r -m -u 1000 -g emqx emqx;
# Tue, 23 May 2023 01:42:43 GMT
ENV EMQX_VERSION=5.0.24
# Tue, 23 May 2023 01:42:43 GMT
ENV AMD64_SHA256=d104bc3e1839447f5ceeaadbb3feb6c604c5f74b07ca33ab4c37baf2a9b33ae3
# Tue, 23 May 2023 01:42:43 GMT
ENV ARM64_SHA256=40d387b7d4dfc4aa7162ef628f25bcb33e8a3fc67740b3cdb5a6d843aa87c2ec
# Tue, 23 May 2023 01:42:43 GMT
ENV LC_ALL=C.UTF-8 LANG=C.UTF-8
# Tue, 23 May 2023 01:42:48 GMT
RUN set -eu;     arch=$(dpkg --print-architecture);     if [ ${arch} = "amd64" ]; then sha256="$AMD64_SHA256"; fi;     if [ ${arch} = "arm64" ]; then sha256="$ARM64_SHA256"; fi;     ID="$(sed -n '/^ID=/p' /etc/os-release | sed -r 's/ID=(.*)/\1/g' | sed 's/\"//g')";     VERSION_ID="$(sed -n '/^VERSION_ID=/p' /etc/os-release | sed -r 's/VERSION_ID=(.*)/\1/g' | sed 's/\"//g')";     pkg="emqx-${EMQX_VERSION}-${ID}${VERSION_ID}-${arch}.tar.gz";     curl -f -O -L https://www.emqx.com/en/downloads/broker/v${EMQX_VERSION}/${pkg} &&     echo "$sha256 *$pkg" | sha256sum -c &&     mkdir /opt/emqx &&     tar zxf $pkg -C /opt/emqx &&     chgrp -Rf emqx /opt/emqx &&     chmod -Rf g+w /opt/emqx &&     chown -Rf emqx /opt/emqx &&     ln -s /opt/emqx/bin/* /usr/local/bin/ &&     rm -f $pkg
# Tue, 23 May 2023 01:42:49 GMT
WORKDIR /opt/emqx
# Tue, 23 May 2023 01:42:49 GMT
USER emqx
# Tue, 23 May 2023 01:42:49 GMT
VOLUME [/opt/emqx/log /opt/emqx/data]
# Tue, 23 May 2023 01:42:49 GMT
EXPOSE 11883 18083 1883 4370 5369 8083 8084 8883
# Tue, 23 May 2023 01:42:49 GMT
COPY file:a75ee173244a77553082438ca14f9a3c739eae012d396b2119540782b95f16bb in /usr/bin/ 
# Tue, 23 May 2023 01:42:49 GMT
ENTRYPOINT ["/usr/bin/docker-entrypoint.sh"]
# Tue, 23 May 2023 01:42:50 GMT
CMD ["/opt/emqx/bin/emqx" "foreground"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8345ceedc06f3b0ae12a8eb9f0f0e7dd52b3ae9800880811d86f7c26b0651446`  
		Last Modified: Tue, 23 May 2023 01:43:12 GMT  
		Size: 3.0 MB (3002990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b78e6c4890d65e6f6f17dbd7faa9d396eaad9d65dd2bbeb2e49aee524b18b1e`  
		Last Modified: Tue, 23 May 2023 01:43:11 GMT  
		Size: 4.1 KB (4115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f3928ab53fc1ed36f55e43718a8e82fdc4b572ff52ec108e1cc737d144d1f63`  
		Last Modified: Tue, 23 May 2023 01:43:18 GMT  
		Size: 68.4 MB (68360170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7629c5a6040608e24f6cca4a4a2dd9e31e4baa54d425e39557dc3c38d6204758`  
		Last Modified: Tue, 23 May 2023 01:43:15 GMT  
		Size: 903.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
