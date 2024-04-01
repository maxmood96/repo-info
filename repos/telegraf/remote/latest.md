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
