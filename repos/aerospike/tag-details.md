<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `aerospike`

-	[`aerospike:4.6.0.13`](#aerospike46013)
-	[`aerospike:4.7.0.11`](#aerospike47011)
-	[`aerospike:4.8.0.6`](#aerospike4806)
-	[`aerospike:latest`](#aerospikelatest)

## `aerospike:4.6.0.13`

```console
$ docker pull aerospike@sha256:81d99b0d0c7a2705342711f46b0aeaba6605913f35e52a821cf8701cdd52652c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.6.0.13` - linux; amd64

```console
$ docker pull aerospike@sha256:f0f9f3c2a6d3687ead017a3dc5444efdb68067c085de3670a5948a978cbc0578
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51645924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d06c77829a568fdbea2080da389ac5659c0d56b3a3574e882463947060a7d21`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Mon, 09 Mar 2020 22:19:28 GMT
ENV AEROSPIKE_VERSION=4.6.0.13
# Mon, 09 Mar 2020 22:19:28 GMT
ENV AEROSPIKE_SHA256=83b6c81922a4dbb17f979a3dd1810f11e4a1f1876093473e469500cde5fd89d6
# Mon, 09 Mar 2020 22:19:45 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 09 Mar 2020 22:19:45 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 09 Mar 2020 22:19:45 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 09 Mar 2020 22:19:46 GMT
VOLUME [/opt/aerospike/data]
# Mon, 09 Mar 2020 22:19:46 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 09 Mar 2020 22:19:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2020 22:19:46 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09251259ccb425f87d38b7dee120aef659d697d18fd24326138f7c237f13395b`  
		Last Modified: Mon, 09 Mar 2020 22:21:00 GMT  
		Size: 29.1 MB (29130543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce154034307da92434542fda05905f2db4f364caf41c04ae5b253187d50dc09`  
		Last Modified: Mon, 09 Mar 2020 22:20:39 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e373b2c41b0a82d920d2b681ec3d619386cfde98f052aeb5eefa228b3ff41c39`  
		Last Modified: Mon, 09 Mar 2020 22:20:40 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.7.0.11`

```console
$ docker pull aerospike@sha256:4cee5c18ab426142f7efdbb45c5e717c1f51a74614cc6ff6b45721d4569e4fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.7.0.11` - linux; amd64

```console
$ docker pull aerospike@sha256:7170cc88aecccf32569c7eed663f7c7de4244f4b3cac7a0e7741d8ccd51b74b0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51770079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77d7ba1dac9a753078ad19d9fd6bf49d627fe9b7539e477b18ebb03991bf899f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Mon, 09 Mar 2020 22:19:52 GMT
ENV AEROSPIKE_VERSION=4.7.0.11
# Mon, 09 Mar 2020 22:19:52 GMT
ENV AEROSPIKE_SHA256=69585f4b519bf43cb7455360fd2fc81b5095533de59161be703f0658dc6d0c80
# Mon, 09 Mar 2020 22:20:08 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 09 Mar 2020 22:20:09 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 09 Mar 2020 22:20:09 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 09 Mar 2020 22:20:09 GMT
VOLUME [/opt/aerospike/data]
# Mon, 09 Mar 2020 22:20:09 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 09 Mar 2020 22:20:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2020 22:20:09 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dfd0756a287be17692c74df0f2343d30a993a91ebe3b37adc482d65921d893`  
		Last Modified: Mon, 09 Mar 2020 22:21:19 GMT  
		Size: 29.3 MB (29254697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c617f29dbb87412f74ad5fd2c897158024dd696a6780d63fee6bbb679e8b92`  
		Last Modified: Mon, 09 Mar 2020 22:21:04 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adafcc0aa91ec7c7dbb3e7fdabf71fb141431966cd299f6ddf305d29a886ecf`  
		Last Modified: Mon, 09 Mar 2020 22:21:04 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:4.8.0.6`

```console
$ docker pull aerospike@sha256:106986d2ceaabc92465c2d6a2a0e1b25277128760bc22611f40b26f3f9c248a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:4.8.0.6` - linux; amd64

```console
$ docker pull aerospike@sha256:d473166f84caa2ad15e89fed04da3f6b133a1bc522ca4907a9c464d5bf01d27d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51845164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbdcbadf81c6b87e5e4dbd70895f64550df618a892d16be3d1872259752e56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Mon, 09 Mar 2020 22:20:13 GMT
ENV AEROSPIKE_VERSION=4.8.0.6
# Mon, 09 Mar 2020 22:20:13 GMT
ENV AEROSPIKE_SHA256=8794e877abcc68faf3e2ccf461e3d9436343addcdccd3daba1c2e4e9154f8ef3
# Mon, 09 Mar 2020 22:20:29 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 09 Mar 2020 22:20:30 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 09 Mar 2020 22:20:30 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 09 Mar 2020 22:20:30 GMT
VOLUME [/opt/aerospike/data]
# Mon, 09 Mar 2020 22:20:30 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 09 Mar 2020 22:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2020 22:20:31 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b5c68ac2bed929971899a5cd199e795e8d55c91284b8947d0b67b7670d477b`  
		Last Modified: Mon, 09 Mar 2020 22:21:47 GMT  
		Size: 29.3 MB (29329784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0609a1262f16e085038d62561b1c5c9edb28a75bbd53535bfae158990a25337`  
		Last Modified: Mon, 09 Mar 2020 22:21:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e8fabb1be83bac1a46fc9462511cbf0640873906c1c921fad496b3361854d9`  
		Last Modified: Mon, 09 Mar 2020 22:21:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `aerospike:latest`

```console
$ docker pull aerospike@sha256:106986d2ceaabc92465c2d6a2a0e1b25277128760bc22611f40b26f3f9c248a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `aerospike:latest` - linux; amd64

```console
$ docker pull aerospike@sha256:d473166f84caa2ad15e89fed04da3f6b133a1bc522ca4907a9c464d5bf01d27d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51845164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4dbdcbadf81c6b87e5e4dbd70895f64550df618a892d16be3d1872259752e56`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:38 GMT
ADD file:1256c62f77a54c982fdb2790d682049b2ad64c8466466e846f3d33ad1ed4035d in / 
# Wed, 26 Feb 2020 00:41:38 GMT
CMD ["bash"]
# Mon, 09 Mar 2020 22:20:13 GMT
ENV AEROSPIKE_VERSION=4.8.0.6
# Mon, 09 Mar 2020 22:20:13 GMT
ENV AEROSPIKE_SHA256=8794e877abcc68faf3e2ccf461e3d9436343addcdccd3daba1c2e4e9154f8ef3
# Mon, 09 Mar 2020 22:20:29 GMT
RUN apt-get update -y   && apt-get install -y wget python lua5.2 gettext-base   && wget "https://www.aerospike.com/artifacts/aerospike-server-community/${AEROSPIKE_VERSION}/aerospike-server-community-${AEROSPIKE_VERSION}-debian9.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y
# Mon, 09 Mar 2020 22:20:30 GMT
COPY file:b2afebdf574a22640dc0687630172a267f2dc7857e8cd93254039deab3b62213 in /etc/aerospike/aerospike.template.conf 
# Mon, 09 Mar 2020 22:20:30 GMT
COPY file:688bc1b7dea55c1dc5575a99640936049823d07bac5c920bbace2369fbb27428 in /entrypoint.sh 
# Mon, 09 Mar 2020 22:20:30 GMT
VOLUME [/opt/aerospike/data]
# Mon, 09 Mar 2020 22:20:30 GMT
EXPOSE 3000 3001 3002 3003
# Mon, 09 Mar 2020 22:20:30 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Mar 2020 22:20:31 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:6d28e14ab8c85bf8a4331de0667c27d19ef4092b12531eec0334b5c2a1012668`  
		Last Modified: Wed, 26 Feb 2020 00:47:21 GMT  
		Size: 22.5 MB (22513365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b5c68ac2bed929971899a5cd199e795e8d55c91284b8947d0b67b7670d477b`  
		Last Modified: Mon, 09 Mar 2020 22:21:47 GMT  
		Size: 29.3 MB (29329784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0609a1262f16e085038d62561b1c5c9edb28a75bbd53535bfae158990a25337`  
		Last Modified: Mon, 09 Mar 2020 22:21:25 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e8fabb1be83bac1a46fc9462511cbf0640873906c1c921fad496b3361854d9`  
		Last Modified: Mon, 09 Mar 2020 22:21:25 GMT  
		Size: 884.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
