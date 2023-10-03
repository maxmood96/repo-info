<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.0`](#kapacitor170)
-	[`kapacitor:1.7.0-alpine`](#kapacitor170-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:5c9a98d80527b5505ae0722278c8a5cc456a089a3bf4cb0a18eb0b601e3ba156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:b37606c4ac1a3eab4291c54449c4d926a1c81501099f26eec0539b492478b0c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134922396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3df09de09d924f50213b85420f250449db847acf4a93d4ee80c55ec2bf22ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 04:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:21:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 07:21:33 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 03 Oct 2023 07:21:40 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 07:21:40 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 07:21:40 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 07:21:40 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 07:21:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 07:21:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 07:21:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ad5fa151345a37245301e58d80e66dff497fa6881342a464fbe2ecb12dc61c`  
		Last Modified: Tue, 03 Oct 2023 05:08:42 GMT  
		Size: 7.1 MB (7120048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a57cbdf0fe7dfb2197dc2b92c76aee687782482fe13163157eb9dd2db9eb`  
		Last Modified: Tue, 03 Oct 2023 07:22:12 GMT  
		Size: 31.7 MB (31688360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5f66460531bd9486d87cf1c06aa0bb9eb215c6265fc0f97155419be5f8636`  
		Last Modified: Tue, 03 Oct 2023 07:22:16 GMT  
		Size: 65.7 MB (65672662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384444177c7816489ef3e25891924ac1bc8880023e087e64fe3b1afd2fccea3`  
		Last Modified: Tue, 03 Oct 2023 07:22:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313a94b3034b1fbd225726cbfe341b82f93be900ace5e620d6a3e53e49e1e257`  
		Last Modified: Tue, 03 Oct 2023 07:22:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5e0f5aec165270eae1700fe7ab521e7ea13d527bd4c2d4be2b8a0d30ea43d680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126715989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec675b3fcf08331d516d073ad66f6282ca22f2580b3e5c386e292d6af2a1170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:10:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 09:10:53 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 03 Oct 2023 09:10:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 09:11:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 09:11:00 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 09:11:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 09:11:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 09:11:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 09:11:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0d5ac6dcf3eaf62ba76d5ddc84c80e68218137512b65ff2533824f3af4788`  
		Last Modified: Tue, 03 Oct 2023 06:22:38 GMT  
		Size: 7.1 MB (7066673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4161b0a34f38f7f422ed4df476cf23843069bb438c59f0aab3b23c25b1c9500`  
		Last Modified: Tue, 03 Oct 2023 09:11:20 GMT  
		Size: 29.6 MB (29586040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7facb4692602daf2ad9dd9d6b935561373942f3c7ba6cc25341711335f0918`  
		Last Modified: Tue, 03 Oct 2023 09:11:25 GMT  
		Size: 61.7 MB (61670748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82edcdc44b2f44e6387e03664b102706fe2f032229e114a82c02040938099969`  
		Last Modified: Tue, 03 Oct 2023 09:11:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6deb278e84693c62658166e919eb5b378678c36721241e4488ed7ccbe046a70`  
		Last Modified: Tue, 03 Oct 2023 09:11:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:5c9a98d80527b5505ae0722278c8a5cc456a089a3bf4cb0a18eb0b601e3ba156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:b37606c4ac1a3eab4291c54449c4d926a1c81501099f26eec0539b492478b0c6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.9 MB (134922396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3df09de09d924f50213b85420f250449db847acf4a93d4ee80c55ec2bf22ff`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 04:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:21:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 07:21:33 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 03 Oct 2023 07:21:40 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 07:21:40 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 07:21:40 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 07:21:40 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 07:21:40 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 07:21:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 07:21:40 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ad5fa151345a37245301e58d80e66dff497fa6881342a464fbe2ecb12dc61c`  
		Last Modified: Tue, 03 Oct 2023 05:08:42 GMT  
		Size: 7.1 MB (7120048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a57cbdf0fe7dfb2197dc2b92c76aee687782482fe13163157eb9dd2db9eb`  
		Last Modified: Tue, 03 Oct 2023 07:22:12 GMT  
		Size: 31.7 MB (31688360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee5f66460531bd9486d87cf1c06aa0bb9eb215c6265fc0f97155419be5f8636`  
		Last Modified: Tue, 03 Oct 2023 07:22:16 GMT  
		Size: 65.7 MB (65672662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5384444177c7816489ef3e25891924ac1bc8880023e087e64fe3b1afd2fccea3`  
		Last Modified: Tue, 03 Oct 2023 07:22:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:313a94b3034b1fbd225726cbfe341b82f93be900ace5e620d6a3e53e49e1e257`  
		Last Modified: Tue, 03 Oct 2023 07:22:08 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:5e0f5aec165270eae1700fe7ab521e7ea13d527bd4c2d4be2b8a0d30ea43d680
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126715989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec675b3fcf08331d516d073ad66f6282ca22f2580b3e5c386e292d6af2a1170`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:10:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 09:10:53 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 03 Oct 2023 09:10:59 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 09:11:00 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 09:11:00 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 09:11:00 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 09:11:00 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 09:11:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 09:11:00 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0d5ac6dcf3eaf62ba76d5ddc84c80e68218137512b65ff2533824f3af4788`  
		Last Modified: Tue, 03 Oct 2023 06:22:38 GMT  
		Size: 7.1 MB (7066673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4161b0a34f38f7f422ed4df476cf23843069bb438c59f0aab3b23c25b1c9500`  
		Last Modified: Tue, 03 Oct 2023 09:11:20 GMT  
		Size: 29.6 MB (29586040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7facb4692602daf2ad9dd9d6b935561373942f3c7ba6cc25341711335f0918`  
		Last Modified: Tue, 03 Oct 2023 09:11:25 GMT  
		Size: 61.7 MB (61670748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82edcdc44b2f44e6387e03664b102706fe2f032229e114a82c02040938099969`  
		Last Modified: Tue, 03 Oct 2023 09:11:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6deb278e84693c62658166e919eb5b378678c36721241e4488ed7ccbe046a70`  
		Last Modified: Tue, 03 Oct 2023 09:11:18 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:649a97fc6725f8320bc780e9559dadcbbae8b97e1bbed5d859e193b35f276b25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:7b7418906094f3e66553c595956ece066860539debed2172bd0e97ccaf6b03ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68673465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c0ab4b2e7a3e604797ddf2015c7b97fcdee7df4948f525dd75b3b8bebc96e8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:31 GMT
ADD file:76d829bbce3dd420a8419919b0916c0fda917011d1e6752ca5b9e53d5ca890a6 in / 
# Mon, 07 Aug 2023 19:20:31 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 02:06:43 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Wed, 09 Aug 2023 02:06:44 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Wed, 09 Aug 2023 02:06:44 GMT
ENV KAPACITOR_VERSION=1.6.6
# Wed, 09 Aug 2023 02:06:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 09 Aug 2023 02:06:52 GMT
EXPOSE 9092
# Wed, 09 Aug 2023 02:06:52 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 09 Aug 2023 02:06:52 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Wed, 09 Aug 2023 02:06:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Aug 2023 02:06:53 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:659d66d51139e8abad819d17e5d3c45eb82e88b9fc588c4de7711f251309b9d2`  
		Last Modified: Mon, 07 Aug 2023 19:21:19 GMT  
		Size: 2.8 MB (2807683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61398f0c26e32fcf30f1436e94600012d7b35bbf04bb4a0cf0304cf2d8ae065f`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc02a84aa2e93219dad782abd5562f8d465bed2fb7769681d5c6a42a87db231`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 284.9 KB (284895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687f33019eea09dc53b5214c7b87d0c9bcb9a3898ad6ee9f316d7865c71c673`  
		Last Modified: Wed, 09 Aug 2023 02:07:16 GMT  
		Size: 65.6 MB (65580154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b00ae2bb82d25948398d6dcea1533849cc768d89ad5a61cd6ecf685c217b2fb`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eedb4317a123bd4dc6bb77c19a0f1ce1410a13a8926df49193aab5f9aecb78e3`  
		Last Modified: Wed, 09 Aug 2023 02:07:08 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:a61c4e620f61fd3c17e1f1245dcbb39802946030aa7ab2b70d34172a89ef61b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:3a2b45d5e51b17e229f8d9c46bbcf24cfc5f60aa76603f841bcec370dce21422
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135969639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e234da8e3bbdd32a4bfda6b6477d98feb8cef36779dbe5f4f5c8ea3a44f036a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 04:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:21:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 07:21:46 GMT
ENV KAPACITOR_VERSION=1.7.0
# Tue, 03 Oct 2023 07:21:54 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 07:21:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 07:21:54 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 07:21:54 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 07:21:54 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 07:21:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 07:21:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ad5fa151345a37245301e58d80e66dff497fa6881342a464fbe2ecb12dc61c`  
		Last Modified: Tue, 03 Oct 2023 05:08:42 GMT  
		Size: 7.1 MB (7120048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a57cbdf0fe7dfb2197dc2b92c76aee687782482fe13163157eb9dd2db9eb`  
		Last Modified: Tue, 03 Oct 2023 07:22:12 GMT  
		Size: 31.7 MB (31688360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922096918bfc8a20ce7617ccb7309bd2c403882094ebe94683ea84da9ffcba22`  
		Last Modified: Tue, 03 Oct 2023 07:22:34 GMT  
		Size: 66.7 MB (66719906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2977095f16835b3c54b9e5e99d87273dbf5e945185e5184376b9477cf7ff320`  
		Last Modified: Tue, 03 Oct 2023 07:22:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f81174504b0f70455c059d561935c512b29411c5240b63b75ab034cdc5756a4`  
		Last Modified: Tue, 03 Oct 2023 07:22:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:740a8612bd985c37f497b5606ee38c27e931f7edc9c8ec88bd2c04e479e831f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127325591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b90b964385719532f13809c09f791c839185de7b5034d82233f148595929bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:10:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 09:11:03 GMT
ENV KAPACITOR_VERSION=1.7.0
# Tue, 03 Oct 2023 09:11:07 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 09:11:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 09:11:08 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 09:11:08 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 09:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 09:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 09:11:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0d5ac6dcf3eaf62ba76d5ddc84c80e68218137512b65ff2533824f3af4788`  
		Last Modified: Tue, 03 Oct 2023 06:22:38 GMT  
		Size: 7.1 MB (7066673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4161b0a34f38f7f422ed4df476cf23843069bb438c59f0aab3b23c25b1c9500`  
		Last Modified: Tue, 03 Oct 2023 09:11:20 GMT  
		Size: 29.6 MB (29586040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bca927ec1b6f5a03d79d4d376b159b10cd32279d2d7260728ee5869f3247f8`  
		Last Modified: Tue, 03 Oct 2023 09:11:39 GMT  
		Size: 62.3 MB (62280350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a439c28f4384f46548166da6d523a327b0678e4d4209278d132617149719446b`  
		Last Modified: Tue, 03 Oct 2023 09:11:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f7beb525193e721c3371ec767203de321bd5f2dac5cc6e1f931c26423dccb1`  
		Last Modified: Tue, 03 Oct 2023 09:11:33 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:0f1c393a6e3fa11feae973703969333e1d506439ca4de5d55848832ef69912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:33a8f10c30c5e5f62585eeac00d1cc0715d9a41bc964378366fea3f7d0a13173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70331993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3853cbb605f2244f62acfb55c54ff149c71bd053238ab42b74a2a09f744bcce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 28 Sep 2023 23:22:11 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Sep 2023 23:22:11 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 28 Sep 2023 23:22:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Sep 2023 23:22:20 GMT
EXPOSE 9092
# Thu, 28 Sep 2023 23:22:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Sep 2023 23:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Sep 2023 23:22:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f6d483e0e31120bd02f44a884174729150927274ce02af767e9f420bf1086`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8a5dcd1f5f2dd9ebf473eb0cc6efa928dcbe492ff45e983de648f06ae6dd14`  
		Last Modified: Thu, 28 Sep 2023 23:22:44 GMT  
		Size: 66.6 MB (66644596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d72cc490ab8065bdc237bcc304fbd0ea8ba3d4afbfcb2fcad365f374a2a6fab`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d09f60f4ac443b6c1c9c30ca7004906aad8263902298d5dd7dd9dca37d8e8`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.0`

```console
$ docker pull kapacitor@sha256:a61c4e620f61fd3c17e1f1245dcbb39802946030aa7ab2b70d34172a89ef61b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:1.7.0` - linux; amd64

```console
$ docker pull kapacitor@sha256:3a2b45d5e51b17e229f8d9c46bbcf24cfc5f60aa76603f841bcec370dce21422
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135969639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e234da8e3bbdd32a4bfda6b6477d98feb8cef36779dbe5f4f5c8ea3a44f036a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 04:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:21:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 07:21:46 GMT
ENV KAPACITOR_VERSION=1.7.0
# Tue, 03 Oct 2023 07:21:54 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 07:21:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 07:21:54 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 07:21:54 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 07:21:54 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 07:21:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 07:21:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ad5fa151345a37245301e58d80e66dff497fa6881342a464fbe2ecb12dc61c`  
		Last Modified: Tue, 03 Oct 2023 05:08:42 GMT  
		Size: 7.1 MB (7120048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a57cbdf0fe7dfb2197dc2b92c76aee687782482fe13163157eb9dd2db9eb`  
		Last Modified: Tue, 03 Oct 2023 07:22:12 GMT  
		Size: 31.7 MB (31688360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922096918bfc8a20ce7617ccb7309bd2c403882094ebe94683ea84da9ffcba22`  
		Last Modified: Tue, 03 Oct 2023 07:22:34 GMT  
		Size: 66.7 MB (66719906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2977095f16835b3c54b9e5e99d87273dbf5e945185e5184376b9477cf7ff320`  
		Last Modified: Tue, 03 Oct 2023 07:22:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f81174504b0f70455c059d561935c512b29411c5240b63b75ab034cdc5756a4`  
		Last Modified: Tue, 03 Oct 2023 07:22:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:1.7.0` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:740a8612bd985c37f497b5606ee38c27e931f7edc9c8ec88bd2c04e479e831f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127325591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b90b964385719532f13809c09f791c839185de7b5034d82233f148595929bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:10:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 09:11:03 GMT
ENV KAPACITOR_VERSION=1.7.0
# Tue, 03 Oct 2023 09:11:07 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 09:11:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 09:11:08 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 09:11:08 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 09:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 09:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 09:11:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0d5ac6dcf3eaf62ba76d5ddc84c80e68218137512b65ff2533824f3af4788`  
		Last Modified: Tue, 03 Oct 2023 06:22:38 GMT  
		Size: 7.1 MB (7066673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4161b0a34f38f7f422ed4df476cf23843069bb438c59f0aab3b23c25b1c9500`  
		Last Modified: Tue, 03 Oct 2023 09:11:20 GMT  
		Size: 29.6 MB (29586040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bca927ec1b6f5a03d79d4d376b159b10cd32279d2d7260728ee5869f3247f8`  
		Last Modified: Tue, 03 Oct 2023 09:11:39 GMT  
		Size: 62.3 MB (62280350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a439c28f4384f46548166da6d523a327b0678e4d4209278d132617149719446b`  
		Last Modified: Tue, 03 Oct 2023 09:11:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f7beb525193e721c3371ec767203de321bd5f2dac5cc6e1f931c26423dccb1`  
		Last Modified: Tue, 03 Oct 2023 09:11:33 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:1.7.0-alpine`

```console
$ docker pull kapacitor@sha256:0f1c393a6e3fa11feae973703969333e1d506439ca4de5d55848832ef69912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:1.7.0-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:33a8f10c30c5e5f62585eeac00d1cc0715d9a41bc964378366fea3f7d0a13173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70331993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3853cbb605f2244f62acfb55c54ff149c71bd053238ab42b74a2a09f744bcce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 28 Sep 2023 23:22:11 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Sep 2023 23:22:11 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 28 Sep 2023 23:22:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Sep 2023 23:22:20 GMT
EXPOSE 9092
# Thu, 28 Sep 2023 23:22:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Sep 2023 23:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Sep 2023 23:22:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f6d483e0e31120bd02f44a884174729150927274ce02af767e9f420bf1086`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8a5dcd1f5f2dd9ebf473eb0cc6efa928dcbe492ff45e983de648f06ae6dd14`  
		Last Modified: Thu, 28 Sep 2023 23:22:44 GMT  
		Size: 66.6 MB (66644596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d72cc490ab8065bdc237bcc304fbd0ea8ba3d4afbfcb2fcad365f374a2a6fab`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d09f60f4ac443b6c1c9c30ca7004906aad8263902298d5dd7dd9dca37d8e8`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:0f1c393a6e3fa11feae973703969333e1d506439ca4de5d55848832ef69912a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:33a8f10c30c5e5f62585eeac00d1cc0715d9a41bc964378366fea3f7d0a13173
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70331993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3853cbb605f2244f62acfb55c54ff149c71bd053238ab42b74a2a09f744bcce`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:22:10 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Thu, 28 Sep 2023 23:22:11 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Thu, 28 Sep 2023 23:22:11 GMT
ENV KAPACITOR_VERSION=1.7.0
# Thu, 28 Sep 2023 23:22:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-v${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 28 Sep 2023 23:22:20 GMT
EXPOSE 9092
# Thu, 28 Sep 2023 23:22:20 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 28 Sep 2023 23:22:20 GMT
COPY file:a64543022a380a96e18ddc4e841e034238df340064743d570fa109d5086b123a in /entrypoint.sh 
# Thu, 28 Sep 2023 23:22:21 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 28 Sep 2023 23:22:21 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3779175f54086809f96dd5b117ed71f84dd847e86676070c520eaf459fa4e08a`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877f6d483e0e31120bd02f44a884174729150927274ce02af767e9f420bf1086`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 284.7 KB (284699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8a5dcd1f5f2dd9ebf473eb0cc6efa928dcbe492ff45e983de648f06ae6dd14`  
		Last Modified: Thu, 28 Sep 2023 23:22:44 GMT  
		Size: 66.6 MB (66644596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d72cc490ab8065bdc237bcc304fbd0ea8ba3d4afbfcb2fcad365f374a2a6fab`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:485d09f60f4ac443b6c1c9c30ca7004906aad8263902298d5dd7dd9dca37d8e8`  
		Last Modified: Thu, 28 Sep 2023 23:22:36 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:a61c4e620f61fd3c17e1f1245dcbb39802946030aa7ab2b70d34172a89ef61b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:3a2b45d5e51b17e229f8d9c46bbcf24cfc5f60aa76603f841bcec370dce21422
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135969639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e234da8e3bbdd32a4bfda6b6477d98feb8cef36779dbe5f4f5c8ea3a44f036a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 04:55:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 07:21:32 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 07:21:46 GMT
ENV KAPACITOR_VERSION=1.7.0
# Tue, 03 Oct 2023 07:21:54 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 07:21:54 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 07:21:54 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 07:21:54 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 07:21:54 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 07:21:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 07:21:55 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ad5fa151345a37245301e58d80e66dff497fa6881342a464fbe2ecb12dc61c`  
		Last Modified: Tue, 03 Oct 2023 05:08:42 GMT  
		Size: 7.1 MB (7120048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4604a57cbdf0fe7dfb2197dc2b92c76aee687782482fe13163157eb9dd2db9eb`  
		Last Modified: Tue, 03 Oct 2023 07:22:12 GMT  
		Size: 31.7 MB (31688360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922096918bfc8a20ce7617ccb7309bd2c403882094ebe94683ea84da9ffcba22`  
		Last Modified: Tue, 03 Oct 2023 07:22:34 GMT  
		Size: 66.7 MB (66719906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2977095f16835b3c54b9e5e99d87273dbf5e945185e5184376b9477cf7ff320`  
		Last Modified: Tue, 03 Oct 2023 07:22:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f81174504b0f70455c059d561935c512b29411c5240b63b75ab034cdc5756a4`  
		Last Modified: Tue, 03 Oct 2023 07:22:26 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:740a8612bd985c37f497b5606ee38c27e931f7edc9c8ec88bd2c04e479e831f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.3 MB (127325591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b90b964385719532f13809c09f791c839185de7b5034d82233f148595929bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:14:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 09:10:53 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Tue, 03 Oct 2023 09:11:03 GMT
ENV KAPACITOR_VERSION=1.7.0
# Tue, 03 Oct 2023 09:11:07 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Tue, 03 Oct 2023 09:11:08 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Tue, 03 Oct 2023 09:11:08 GMT
EXPOSE 9092
# Tue, 03 Oct 2023 09:11:08 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 03 Oct 2023 09:11:09 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Tue, 03 Oct 2023 09:11:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 03 Oct 2023 09:11:09 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc0d5ac6dcf3eaf62ba76d5ddc84c80e68218137512b65ff2533824f3af4788`  
		Last Modified: Tue, 03 Oct 2023 06:22:38 GMT  
		Size: 7.1 MB (7066673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4161b0a34f38f7f422ed4df476cf23843069bb438c59f0aab3b23c25b1c9500`  
		Last Modified: Tue, 03 Oct 2023 09:11:20 GMT  
		Size: 29.6 MB (29586040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bca927ec1b6f5a03d79d4d376b159b10cd32279d2d7260728ee5869f3247f8`  
		Last Modified: Tue, 03 Oct 2023 09:11:39 GMT  
		Size: 62.3 MB (62280350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a439c28f4384f46548166da6d523a327b0678e4d4209278d132617149719446b`  
		Last Modified: Tue, 03 Oct 2023 09:11:33 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f7beb525193e721c3371ec767203de321bd5f2dac5cc6e1f931c26423dccb1`  
		Last Modified: Tue, 03 Oct 2023 09:11:33 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
