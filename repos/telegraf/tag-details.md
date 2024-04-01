<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.28`](#telegraf128)
-	[`telegraf:1.28-alpine`](#telegraf128-alpine)
-	[`telegraf:1.28.5`](#telegraf1285)
-	[`telegraf:1.28.5-alpine`](#telegraf1285-alpine)
-	[`telegraf:1.29`](#telegraf129)
-	[`telegraf:1.29-alpine`](#telegraf129-alpine)
-	[`telegraf:1.29.5`](#telegraf1295)
-	[`telegraf:1.29.5-alpine`](#telegraf1295-alpine)
-	[`telegraf:1.30`](#telegraf130)
-	[`telegraf:1.30-alpine`](#telegraf130-alpine)
-	[`telegraf:1.30.1`](#telegraf1301)
-	[`telegraf:1.30.1-alpine`](#telegraf1301-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:9a770d65780042542dd14dc7b91480db0cf4480381c4ad78253fd79ee581059c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:00184c200088021aa263dd2224fc4dddcb7a4cdb9495a6b422125a2ecd772ae7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149841779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4946b79464c394c395462fe39c5eb94abc6ac110c720950532e2068e2196ad2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 16:06:52 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 12 Mar 2024 16:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 16:06:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:29:40 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:29:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8ef7abfe7d8db1d4690476b48351fa066c6fc838f2c9793d4d6a2243ce8e`  
		Last Modified: Tue, 12 Mar 2024 16:07:47 GMT  
		Size: 57.1 MB (57089120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb3d3c1e3db320e3b44fae4b1b216e721127c8a5355a5988bde67ce94b03661`  
		Last Modified: Thu, 14 Mar 2024 20:30:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:63c045dd910821b0c2ad0a6a8d723de1626295bcd5724da768640053cf25104c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137589902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b38966648f1ba8b14a4bfda1a5998190e6d733a800cc3e43b8e974d3a61263`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:44:17 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 12 Mar 2024 10:44:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:44:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:30:54 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:30:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:30:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ada91f82a888edcad63bd068a71938347f11e7b317baa0ef6e83e0e413122f7`  
		Last Modified: Tue, 12 Mar 2024 10:45:22 GMT  
		Size: 52.6 MB (52554629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075940d49ced4b6ca4c53b7b8ae4837578c95155decb0f347b8bd98901ecceee`  
		Last Modified: Thu, 14 Mar 2024 20:31:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:78549ecc7fafaf7e3da97fb9bd796f949a92e8a0a73f2fc7eef0517dd81692b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144001833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c42ee3bc2a9449b51b01708225bba03654661eee32e753b014b4331a38bdbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:41:28 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 12 Mar 2024 10:41:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:41:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:16:09 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:16:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:16:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71b0735072bae580257ab18789c2e82f2c2fb2b1ece2e43f6fae546aff7941`  
		Last Modified: Tue, 12 Mar 2024 10:42:20 GMT  
		Size: 51.8 MB (51750666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e337f78bb523e97b92c911a4d58a8b3eadddfdf21fc87e8e06912a80def5c0f3`  
		Last Modified: Thu, 14 Mar 2024 20:16:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:57bc33034b6d4d6a96f731b8265a2c9b3985311060ce359879b0fd6ae9b43c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f7029c882a1e0d8dcba490bac1e95c52907200b5be69479a501eba9d9bd93475
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62934041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7687f8b8bb846071a28467f7e04ee14b36738636e4c07cac62275932bac3259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:10 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 08:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:17 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc84cbb6d9e3d0bc47ba96808f7dad0ea7ae3dea5956e44a69ad86374660666`  
		Last Modified: Sat, 16 Mar 2024 08:57:07 GMT  
		Size: 56.9 MB (56914244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f389965f1bfc3e1b5beec1fe0af5e3abe25a32310c0f26c303f66e844988f98`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:58b50c2433f9a957d62b40780760df86989c7d7fb6db583f29a82de80c84f609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57629106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ebbf0803b5bb23e9014912e03226a830106c5da0014f838310c29d6c28e512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:47 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 02:41:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:41:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:41:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:41:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:41:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed275664d335915c59116fc4dcb505bd5b0ccd59b112b85c7d0dbecb230b7bd8`  
		Last Modified: Sat, 16 Mar 2024 02:42:40 GMT  
		Size: 51.6 MB (51587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca806e7a7334d09e576e9279db970934609cd4b9ad9828ebcf85b589837195e`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5`

```console
$ docker pull telegraf@sha256:9a770d65780042542dd14dc7b91480db0cf4480381c4ad78253fd79ee581059c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28.5` - linux; amd64

```console
$ docker pull telegraf@sha256:00184c200088021aa263dd2224fc4dddcb7a4cdb9495a6b422125a2ecd772ae7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.8 MB (149841779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4946b79464c394c395462fe39c5eb94abc6ac110c720950532e2068e2196ad2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 16:06:52 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 12 Mar 2024 16:06:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 16:06:57 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:29:40 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:29:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:29:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ff8ef7abfe7d8db1d4690476b48351fa066c6fc838f2c9793d4d6a2243ce8e`  
		Last Modified: Tue, 12 Mar 2024 16:07:47 GMT  
		Size: 57.1 MB (57089120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb3d3c1e3db320e3b44fae4b1b216e721127c8a5355a5988bde67ce94b03661`  
		Last Modified: Thu, 14 Mar 2024 20:30:27 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:63c045dd910821b0c2ad0a6a8d723de1626295bcd5724da768640053cf25104c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.6 MB (137589902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28b38966648f1ba8b14a4bfda1a5998190e6d733a800cc3e43b8e974d3a61263`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:44:17 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 12 Mar 2024 10:44:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:44:25 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:30:54 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:30:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:30:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ada91f82a888edcad63bd068a71938347f11e7b317baa0ef6e83e0e413122f7`  
		Last Modified: Tue, 12 Mar 2024 10:45:22 GMT  
		Size: 52.6 MB (52554629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075940d49ced4b6ca4c53b7b8ae4837578c95155decb0f347b8bd98901ecceee`  
		Last Modified: Thu, 14 Mar 2024 20:31:19 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:78549ecc7fafaf7e3da97fb9bd796f949a92e8a0a73f2fc7eef0517dd81692b5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144001833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c42ee3bc2a9449b51b01708225bba03654661eee32e753b014b4331a38bdbc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:41:28 GMT
ENV TELEGRAF_VERSION=1.28.5
# Tue, 12 Mar 2024 10:41:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:41:35 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:16:09 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:16:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:16:09 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e71b0735072bae580257ab18789c2e82f2c2fb2b1ece2e43f6fae546aff7941`  
		Last Modified: Tue, 12 Mar 2024 10:42:20 GMT  
		Size: 51.8 MB (51750666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e337f78bb523e97b92c911a4d58a8b3eadddfdf21fc87e8e06912a80def5c0f3`  
		Last Modified: Thu, 14 Mar 2024 20:16:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.5-alpine`

```console
$ docker pull telegraf@sha256:57bc33034b6d4d6a96f731b8265a2c9b3985311060ce359879b0fd6ae9b43c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:f7029c882a1e0d8dcba490bac1e95c52907200b5be69479a501eba9d9bd93475
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62934041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7687f8b8bb846071a28467f7e04ee14b36738636e4c07cac62275932bac3259`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:10 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 08:56:17 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:17 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:17 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:17 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc84cbb6d9e3d0bc47ba96808f7dad0ea7ae3dea5956e44a69ad86374660666`  
		Last Modified: Sat, 16 Mar 2024 08:57:07 GMT  
		Size: 56.9 MB (56914244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f389965f1bfc3e1b5beec1fe0af5e3abe25a32310c0f26c303f66e844988f98`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:58b50c2433f9a957d62b40780760df86989c7d7fb6db583f29a82de80c84f609
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57629106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2ebbf0803b5bb23e9014912e03226a830106c5da0014f838310c29d6c28e512`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:47 GMT
ENV TELEGRAF_VERSION=1.28.5
# Sat, 16 Mar 2024 02:41:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:41:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:41:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:41:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:41:55 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed275664d335915c59116fc4dcb505bd5b0ccd59b112b85c7d0dbecb230b7bd8`  
		Last Modified: Sat, 16 Mar 2024 02:42:40 GMT  
		Size: 51.6 MB (51587851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca806e7a7334d09e576e9279db970934609cd4b9ad9828ebcf85b589837195e`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29`

```console
$ docker pull telegraf@sha256:31f052289bd17932fc0dc389208f92d7ecd81df26f1a49fed01b9915327a2e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29` - linux; amd64

```console
$ docker pull telegraf@sha256:d7e29caff336112af0e7a6cd9cf9407814bf3f68c46980324a00211e48a1e430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b8c11dff8ce5af2891ca49340965fafa6c9f8a93f381b1e37dff9973c5cec5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 16:07:02 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 12 Mar 2024 16:07:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 16:07:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:29:54 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:29:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:29:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4313a9c773dd18aa516bb340d1d3a57d75dcd775fb87750307dcdd6571dad86c`  
		Last Modified: Tue, 12 Mar 2024 16:08:07 GMT  
		Size: 62.6 MB (62642639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db71429a79977002d4be1f005436de9ba407ce480d25607661637707d43dc14`  
		Last Modified: Thu, 14 Mar 2024 20:30:52 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ffcd3a7e7b6d5625b22f9820863ca89e9bbe29a7529185171cf6e8aacd7b9f8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143020697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05048471fe3ff9b08dda3f9fc7c325c9673b3b3841105ffdb76096bb2bd0d179`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:44:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 12 Mar 2024 10:44:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:44:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:30:56 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:30:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:30:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6c2316a2ac3d33ff4b85748dc3ed745908556ba78faa759ab020620c6e3fc3`  
		Last Modified: Tue, 12 Mar 2024 10:45:42 GMT  
		Size: 58.0 MB (57985422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488c6563f1fa7c340f76daba909d3d015249193e399b97fa84997495d899460`  
		Last Modified: Thu, 14 Mar 2024 20:31:28 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5e21df215f950448a121b09957a419792fda65af4b6861ef35a1528ff16cac52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c4e5fed35f444f2b2887717d3cf34dbf45c4fdff43eca7e722dcb3330ed3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:41:39 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 12 Mar 2024 10:41:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:41:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:16:22 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:16:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:16:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550eb4f8ff5e207b1c8fa25b95b57e7c01529bdafc54a4d6165fca525d444e67`  
		Last Modified: Tue, 12 Mar 2024 10:42:34 GMT  
		Size: 57.0 MB (56981324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ee426afecd056730e9e3b7f0bb5d9df249c00d055f634a37ad36b57e9c76a`  
		Last Modified: Thu, 14 Mar 2024 20:17:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29-alpine`

```console
$ docker pull telegraf@sha256:e7189e5fc22b61e1141016ef9e4e3577caada65c8a26544074259f30a1ad9d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:823a2e316bd3af03d98183c4578af04a0ec9b2e06c98fea702f6de057eafc3fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68477324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd48b205b097d2394b0f2fc0fbe817e35c206890692d30ae95bb45358cc50c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:22 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 08:56:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512bc4fc4e3f7b669e009a477ad623af9023db4fcbd9ace2be72ab1d91936d3`  
		Last Modified: Sat, 16 Mar 2024 08:57:25 GMT  
		Size: 62.5 MB (62457526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576d31c8349e3d3dae1c2edf7078657d76c6e3c4a2faee5168f8a20c8c2bc0ab`  
		Last Modified: Sat, 16 Mar 2024 08:57:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a7bed99c8e39b5eebaaa167953481466e7389b4c1b6c4f6774a55b840de5fbdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62839803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7ba5175eb0179c5c2014027104e9e056df19ce22192b09c92cf96c4c9a96e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:58 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 02:42:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:42:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:42:06 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:42:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:42:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1affe1933624c96f8732c646cd6e3ddf57d1202cb43246455d627df374eaf266`  
		Last Modified: Sat, 16 Mar 2024 02:42:55 GMT  
		Size: 56.8 MB (56798544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceff9497b8bf1af89729eff827aa454ef369d6faa5772a8c3e296c790b11e6e`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.5`

```console
$ docker pull telegraf@sha256:31f052289bd17932fc0dc389208f92d7ecd81df26f1a49fed01b9915327a2e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.29.5` - linux; amd64

```console
$ docker pull telegraf@sha256:d7e29caff336112af0e7a6cd9cf9407814bf3f68c46980324a00211e48a1e430
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155395296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b8c11dff8ce5af2891ca49340965fafa6c9f8a93f381b1e37dff9973c5cec5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 16:07:02 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 12 Mar 2024 16:07:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 16:07:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:29:54 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:29:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:29:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4313a9c773dd18aa516bb340d1d3a57d75dcd775fb87750307dcdd6571dad86c`  
		Last Modified: Tue, 12 Mar 2024 16:08:07 GMT  
		Size: 62.6 MB (62642639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db71429a79977002d4be1f005436de9ba407ce480d25607661637707d43dc14`  
		Last Modified: Thu, 14 Mar 2024 20:30:52 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ffcd3a7e7b6d5625b22f9820863ca89e9bbe29a7529185171cf6e8aacd7b9f8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (143020697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05048471fe3ff9b08dda3f9fc7c325c9673b3b3841105ffdb76096bb2bd0d179`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:44:29 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 12 Mar 2024 10:44:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:44:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:30:56 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:30:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:30:56 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6c2316a2ac3d33ff4b85748dc3ed745908556ba78faa759ab020620c6e3fc3`  
		Last Modified: Tue, 12 Mar 2024 10:45:42 GMT  
		Size: 58.0 MB (57985422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b488c6563f1fa7c340f76daba909d3d015249193e399b97fa84997495d899460`  
		Last Modified: Thu, 14 Mar 2024 20:31:28 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:5e21df215f950448a121b09957a419792fda65af4b6861ef35a1528ff16cac52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.2 MB (149232491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec8c4e5fed35f444f2b2887717d3cf34dbf45c4fdff43eca7e722dcb3330ed3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Mar 2024 10:41:39 GMT
ENV TELEGRAF_VERSION=1.29.5
# Tue, 12 Mar 2024 10:41:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Tue, 12 Mar 2024 10:41:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 14 Mar 2024 20:16:22 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Thu, 14 Mar 2024 20:16:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 14 Mar 2024 20:16:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:550eb4f8ff5e207b1c8fa25b95b57e7c01529bdafc54a4d6165fca525d444e67`  
		Last Modified: Tue, 12 Mar 2024 10:42:34 GMT  
		Size: 57.0 MB (56981324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8ee426afecd056730e9e3b7f0bb5d9df249c00d055f634a37ad36b57e9c76a`  
		Last Modified: Thu, 14 Mar 2024 20:17:19 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.29.5-alpine`

```console
$ docker pull telegraf@sha256:e7189e5fc22b61e1141016ef9e4e3577caada65c8a26544074259f30a1ad9d0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.29.5-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:823a2e316bd3af03d98183c4578af04a0ec9b2e06c98fea702f6de057eafc3fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68477324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbfd48b205b097d2394b0f2fc0fbe817e35c206890692d30ae95bb45358cc50c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 08:56:22 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 08:56:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 08:56:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 08:56:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 08:56:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 08:56:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4512bc4fc4e3f7b669e009a477ad623af9023db4fcbd9ace2be72ab1d91936d3`  
		Last Modified: Sat, 16 Mar 2024 08:57:25 GMT  
		Size: 62.5 MB (62457526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576d31c8349e3d3dae1c2edf7078657d76c6e3c4a2faee5168f8a20c8c2bc0ab`  
		Last Modified: Sat, 16 Mar 2024 08:57:15 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.29.5-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:a7bed99c8e39b5eebaaa167953481466e7389b4c1b6c4f6774a55b840de5fbdc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62839803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf7ba5175eb0179c5c2014027104e9e056df19ce22192b09c92cf96c4c9a96e4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 16 Mar 2024 02:41:58 GMT
ENV TELEGRAF_VERSION=1.29.5
# Sat, 16 Mar 2024 02:42:05 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 16 Mar 2024 02:42:06 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 16 Mar 2024 02:42:06 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 16 Mar 2024 02:42:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 16 Mar 2024 02:42:06 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1affe1933624c96f8732c646cd6e3ddf57d1202cb43246455d627df374eaf266`  
		Last Modified: Sat, 16 Mar 2024 02:42:55 GMT  
		Size: 56.8 MB (56798544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dceff9497b8bf1af89729eff827aa454ef369d6faa5772a8c3e296c790b11e6e`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30`

```console
$ docker pull telegraf@sha256:86f1455769db511b10df851f7bd4c969d97cd1cf420d6fbaa8bc5f305b9ab53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.30` - linux; amd64

```console
$ docker pull telegraf@sha256:4d48e15322a141a9ecdc60f95d9ee91bbfabb2eca6af89df2f2497439212a2fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154537800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab72a0cd5a92ba844a9cc44b19e92b5b75e1be160be1045291d46ea1cc3058d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 19:52:38 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 19:52:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:43 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b15022dbd7c4e3588f4d4d8e23086cfbcc3e460d4f3df982a660432209e6033`  
		Last Modified: Mon, 01 Apr 2024 19:53:20 GMT  
		Size: 61.8 MB (61785143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c68af842572b05e7616d7e08b50692906cb809cb4354649e3f5a7936a8cc8`  
		Last Modified: Mon, 01 Apr 2024 19:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347fbfd214d2e072564c5947ab72f1e5d87ad3f418f11358b5a7b5227d837dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142211164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18dadc5fdc2703ae2ec57364c556312d4fb40c45058b406ca4cf3a81a96e38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 19:07:11 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:07:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 19:07:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:07:24 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 19:07:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:07:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca44994f4a2c883ad2b4574216acd646b16555d3fc8c56363e33acc9de140a68`  
		Last Modified: Mon, 01 Apr 2024 19:07:52 GMT  
		Size: 57.2 MB (57175889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b394adc11714b5d10f450c9a8237ef957673157c3ce5000121ddb6de481b9426`  
		Last Modified: Mon, 01 Apr 2024 19:07:40 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:16f79775f910a2d8afc700b836394f21649c84a63073e8d523a5dbaf1a4bbaf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148420027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce325075b59dcf16e51946fe3a828603015ac2d4903410c2fc3c1d6fa2d4a50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 20:17:21 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 20:17:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:28 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab68c0651de989b1038a006818d89578d00ef256e2512b5f7e3f5dcd75920c`  
		Last Modified: Mon, 01 Apr 2024 20:18:04 GMT  
		Size: 56.2 MB (56168860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35dd6d6b063572b88ad1c4d63985d420b71befc174e82345775b6d8751115ec`  
		Last Modified: Mon, 01 Apr 2024 20:17:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30-alpine`

```console
$ docker pull telegraf@sha256:2e8da2041a8b3163d6039862aaeacf05420e9cb3dd4d334e96c7dd9971ae85cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.30-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4e1101d6718d7e99d1ceddba0687186a4e76a30a097dbf34e4afda07a99c352a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67628051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e383f3e32d78ad2f6812dd3c8399b2d9e0c757b331b6d13749e5d6e246c916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 01 Apr 2024 19:52:47 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 19:52:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ef348089694c64746be53352084f76ff2a027e870e9e457021132b8f1dab2`  
		Last Modified: Mon, 01 Apr 2024 19:53:42 GMT  
		Size: 61.6 MB (61608255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35baddb4f9c16e6b2d3ee2828cd3f4c2fa8825edfe4e8236547fc43be03bb27`  
		Last Modified: Mon, 01 Apr 2024 19:53:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3395f3b188cccef3c71bba84acac85db53a0c825ef601fce2e91dc63336de281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22374b3bcb08a9cfcd3edd4ffbb5f8d9cdace2870f0927f632c363681e24f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 01 Apr 2024 20:17:30 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:38 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 20:17:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:40 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752fdc06623ef51aa94016d2b9d40e9cbdfda254fc20f531b54ea89eec318b5`  
		Last Modified: Mon, 01 Apr 2024 20:18:22 GMT  
		Size: 56.0 MB (55980774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b481c2fc94ecef71df2522db417d2f34aeac69a34cbcdabed7d6087de34eae4`  
		Last Modified: Mon, 01 Apr 2024 20:18:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30.1`

```console
$ docker pull telegraf@sha256:86f1455769db511b10df851f7bd4c969d97cd1cf420d6fbaa8bc5f305b9ab53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.30.1` - linux; amd64

```console
$ docker pull telegraf@sha256:4d48e15322a141a9ecdc60f95d9ee91bbfabb2eca6af89df2f2497439212a2fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154537800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab72a0cd5a92ba844a9cc44b19e92b5b75e1be160be1045291d46ea1cc3058d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 19:52:38 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 19:52:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:43 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b15022dbd7c4e3588f4d4d8e23086cfbcc3e460d4f3df982a660432209e6033`  
		Last Modified: Mon, 01 Apr 2024 19:53:20 GMT  
		Size: 61.8 MB (61785143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c68af842572b05e7616d7e08b50692906cb809cb4354649e3f5a7936a8cc8`  
		Last Modified: Mon, 01 Apr 2024 19:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30.1` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347fbfd214d2e072564c5947ab72f1e5d87ad3f418f11358b5a7b5227d837dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142211164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18dadc5fdc2703ae2ec57364c556312d4fb40c45058b406ca4cf3a81a96e38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 19:07:11 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:07:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 19:07:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:07:24 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 19:07:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:07:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca44994f4a2c883ad2b4574216acd646b16555d3fc8c56363e33acc9de140a68`  
		Last Modified: Mon, 01 Apr 2024 19:07:52 GMT  
		Size: 57.2 MB (57175889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b394adc11714b5d10f450c9a8237ef957673157c3ce5000121ddb6de481b9426`  
		Last Modified: Mon, 01 Apr 2024 19:07:40 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30.1` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:16f79775f910a2d8afc700b836394f21649c84a63073e8d523a5dbaf1a4bbaf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148420027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce325075b59dcf16e51946fe3a828603015ac2d4903410c2fc3c1d6fa2d4a50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 20:17:21 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 20:17:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:28 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab68c0651de989b1038a006818d89578d00ef256e2512b5f7e3f5dcd75920c`  
		Last Modified: Mon, 01 Apr 2024 20:18:04 GMT  
		Size: 56.2 MB (56168860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35dd6d6b063572b88ad1c4d63985d420b71befc174e82345775b6d8751115ec`  
		Last Modified: Mon, 01 Apr 2024 20:17:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.30.1-alpine`

```console
$ docker pull telegraf@sha256:2e8da2041a8b3163d6039862aaeacf05420e9cb3dd4d334e96c7dd9971ae85cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.30.1-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4e1101d6718d7e99d1ceddba0687186a4e76a30a097dbf34e4afda07a99c352a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67628051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e383f3e32d78ad2f6812dd3c8399b2d9e0c757b331b6d13749e5d6e246c916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 01 Apr 2024 19:52:47 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 19:52:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ef348089694c64746be53352084f76ff2a027e870e9e457021132b8f1dab2`  
		Last Modified: Mon, 01 Apr 2024 19:53:42 GMT  
		Size: 61.6 MB (61608255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35baddb4f9c16e6b2d3ee2828cd3f4c2fa8825edfe4e8236547fc43be03bb27`  
		Last Modified: Mon, 01 Apr 2024 19:53:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.30.1-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3395f3b188cccef3c71bba84acac85db53a0c825ef601fce2e91dc63336de281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22374b3bcb08a9cfcd3edd4ffbb5f8d9cdace2870f0927f632c363681e24f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 01 Apr 2024 20:17:30 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:38 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 20:17:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:40 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752fdc06623ef51aa94016d2b9d40e9cbdfda254fc20f531b54ea89eec318b5`  
		Last Modified: Mon, 01 Apr 2024 20:18:22 GMT  
		Size: 56.0 MB (55980774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b481c2fc94ecef71df2522db417d2f34aeac69a34cbcdabed7d6087de34eae4`  
		Last Modified: Mon, 01 Apr 2024 20:18:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:2e8da2041a8b3163d6039862aaeacf05420e9cb3dd4d334e96c7dd9971ae85cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:4e1101d6718d7e99d1ceddba0687186a4e76a30a097dbf34e4afda07a99c352a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67628051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4e383f3e32d78ad2f6812dd3c8399b2d9e0c757b331b6d13749e5d6e246c916`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 08:56:08 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 08:56:10 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 01 Apr 2024 19:52:47 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:53 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 19:52:54 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:54 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:54 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162ebdf1596ab6dcfd486bee21886e418f16f6c426a8dd266cba7da20b557281`  
		Last Modified: Sat, 16 Mar 2024 08:56:58 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abdd04d97f3dab462dc59e41d85f02932280e01a7d7a2cd1d24c977e5ae0b583`  
		Last Modified: Sat, 16 Mar 2024 08:56:59 GMT  
		Size: 2.6 MB (2610463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7ef348089694c64746be53352084f76ff2a027e870e9e457021132b8f1dab2`  
		Last Modified: Mon, 01 Apr 2024 19:53:42 GMT  
		Size: 61.6 MB (61608255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35baddb4f9c16e6b2d3ee2828cd3f4c2fa8825edfe4e8236547fc43be03bb27`  
		Last Modified: Mon, 01 Apr 2024 19:53:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:3395f3b188cccef3c71bba84acac85db53a0c825ef601fce2e91dc63336de281
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62022034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22374b3bcb08a9cfcd3edd4ffbb5f8d9cdace2870f0927f632c363681e24f05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 02:41:45 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 16 Mar 2024 02:41:47 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Mon, 01 Apr 2024 20:17:30 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:38 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Mon, 01 Apr 2024 20:17:40 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:40 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:40 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2675ee4ddf03252fa477bd14d6e59e0470e73d69c7fb12bade1d12e074715140`  
		Last Modified: Sat, 16 Mar 2024 02:42:34 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870e8831f6d198a84a383f159cec54a3ee90276d6772ca50a61c7cd967628656`  
		Last Modified: Sat, 16 Mar 2024 02:42:35 GMT  
		Size: 2.7 MB (2692939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0752fdc06623ef51aa94016d2b9d40e9cbdfda254fc20f531b54ea89eec318b5`  
		Last Modified: Mon, 01 Apr 2024 20:18:22 GMT  
		Size: 56.0 MB (55980774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b481c2fc94ecef71df2522db417d2f34aeac69a34cbcdabed7d6087de34eae4`  
		Last Modified: Mon, 01 Apr 2024 20:18:14 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:86f1455769db511b10df851f7bd4c969d97cd1cf420d6fbaa8bc5f305b9ab53d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:4d48e15322a141a9ecdc60f95d9ee91bbfabb2eca6af89df2f2497439212a2fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.5 MB (154537800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab72a0cd5a92ba844a9cc44b19e92b5b75e1be160be1045291d46ea1cc3058d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 01:20:46 GMT
ADD file:b18b4c32dd8042f45097997c732dc29b3917fd7d5f337f9e772eee5875fbe6f1 in / 
# Tue, 12 Mar 2024 01:20:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:53:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 16:06:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 19:52:38 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:52:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 19:52:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:52:43 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 19:52:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:52:43 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:71215d55680cf0ab2dcc0e1dd65ed76414e3fb0c294249b5b9319a8fa7c398e4`  
		Last Modified: Tue, 12 Mar 2024 01:25:15 GMT  
		Size: 49.6 MB (49552196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb8f9c23302e175d87a827f0a1c376bd59b1f6949bd3bc24ab8da0d669cdfa0`  
		Last Modified: Tue, 12 Mar 2024 06:02:24 GMT  
		Size: 24.0 MB (24046734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c22ef0767adf5b83c94809eb5ca18788c14fffadd8a347dd3be325c7e12f13`  
		Last Modified: Tue, 12 Mar 2024 16:07:25 GMT  
		Size: 19.2 MB (19151289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bc1a5d3757f542b0029fe62493bf3e1fe1cafae2e8463156597eb5165ecad6`  
		Last Modified: Tue, 12 Mar 2024 16:07:22 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b15022dbd7c4e3588f4d4d8e23086cfbcc3e460d4f3df982a660432209e6033`  
		Last Modified: Mon, 01 Apr 2024 19:53:20 GMT  
		Size: 61.8 MB (61785143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc4c68af842572b05e7616d7e08b50692906cb809cb4354649e3f5a7936a8cc8`  
		Last Modified: Mon, 01 Apr 2024 19:53:11 GMT  
		Size: 622.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7347fbfd214d2e072564c5947ab72f1e5d87ad3f418f11358b5a7b5227d837dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142211164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b18dadc5fdc2703ae2ec57364c556312d4fb40c45058b406ca4cf3a81a96e38`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:04 GMT
ADD file:d6d1b02b31352539820541191f21cf977c521a75fbf0811c773f3cd9e7d4510a in / 
# Tue, 12 Mar 2024 00:59:05 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:09:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:44:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 19:07:11 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 19:07:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 19:07:24 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 19:07:24 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 19:07:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 19:07:25 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:686eee10d9b82edf962cb35763f03fa5708a79495b3175382801f654942520e6`  
		Last Modified: Tue, 12 Mar 2024 01:03:12 GMT  
		Size: 45.2 MB (45153820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c3d658796dfecfb5d51bf076c1e96ee8a080aef7eb8e33612903ba6a9a34ab`  
		Last Modified: Tue, 12 Mar 2024 02:19:06 GMT  
		Size: 22.0 MB (21950303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74481186d24f4cd955c59b1608dcd60faeeabcfed15b83e26be1beb3406c6a9c`  
		Last Modified: Tue, 12 Mar 2024 10:44:57 GMT  
		Size: 17.9 MB (17928713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7114de2be252e285f9a6405029645d9fc97903924f7dd5130ca30c3fd748740b`  
		Last Modified: Tue, 12 Mar 2024 10:44:50 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca44994f4a2c883ad2b4574216acd646b16555d3fc8c56363e33acc9de140a68`  
		Last Modified: Mon, 01 Apr 2024 19:07:52 GMT  
		Size: 57.2 MB (57175889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b394adc11714b5d10f450c9a8237ef957673157c3ce5000121ddb6de481b9426`  
		Last Modified: Mon, 01 Apr 2024 19:07:40 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:16f79775f910a2d8afc700b836394f21649c84a63073e8d523a5dbaf1a4bbaf0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148420027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce325075b59dcf16e51946fe3a828603015ac2d4903410c2fc3c1d6fa2d4a50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:26 GMT
ADD file:9b51ed214f9332acf3126d841440c24eed0beac4062487fb360b288f628454dc in / 
# Tue, 12 Mar 2024 00:45:27 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:24:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 10:41:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 01 Apr 2024 20:17:21 GMT
ENV TELEGRAF_VERSION=1.30.1
# Mon, 01 Apr 2024 20:17:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Mon, 01 Apr 2024 20:17:28 GMT
EXPOSE 8092/udp 8094 8125/udp
# Mon, 01 Apr 2024 20:17:28 GMT
COPY file:3d723e9d10409fb06c7eaa4bbebe18017fc82dee6330d688adb684b64917f206 in /entrypoint.sh 
# Mon, 01 Apr 2024 20:17:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 01 Apr 2024 20:17:29 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:6ee0baa58a3d368515336c1b5c1cade29c975e1b49a832f19e22f4c46f4a23a7`  
		Last Modified: Tue, 12 Mar 2024 00:48:33 GMT  
		Size: 49.6 MB (49590984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992a857ef57584af4efb4c62d68456f1e8513c95d6248fd796a9ea7f45da4d79`  
		Last Modified: Tue, 12 Mar 2024 01:34:28 GMT  
		Size: 23.6 MB (23582876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e407b73af525701d9c544e65ad100cf61ce7b0b35a0668cb84b3793a7cbd87`  
		Last Modified: Tue, 12 Mar 2024 10:42:03 GMT  
		Size: 19.1 MB (19074868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3c36d7d3c443904bea5ff927ab3d19279eb646d843db7a94388887c478a59e`  
		Last Modified: Tue, 12 Mar 2024 10:42:01 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dab68c0651de989b1038a006818d89578d00ef256e2512b5f7e3f5dcd75920c`  
		Last Modified: Mon, 01 Apr 2024 20:18:04 GMT  
		Size: 56.2 MB (56168860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35dd6d6b063572b88ad1c4d63985d420b71befc174e82345775b6d8751115ec`  
		Last Modified: Mon, 01 Apr 2024 20:17:57 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
