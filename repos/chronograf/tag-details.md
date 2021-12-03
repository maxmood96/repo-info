<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.6`](#chronograf16)
-	[`chronograf:1.6-alpine`](#chronograf16-alpine)
-	[`chronograf:1.6.2`](#chronograf162)
-	[`chronograf:1.6.2-alpine`](#chronograf162-alpine)
-	[`chronograf:1.7`](#chronograf17)
-	[`chronograf:1.7-alpine`](#chronograf17-alpine)
-	[`chronograf:1.7.17`](#chronograf1717)
-	[`chronograf:1.7.17-alpine`](#chronograf1717-alpine)
-	[`chronograf:1.8`](#chronograf18)
-	[`chronograf:1.8-alpine`](#chronograf18-alpine)
-	[`chronograf:1.8.10`](#chronograf1810)
-	[`chronograf:1.8.10-alpine`](#chronograf1810-alpine)
-	[`chronograf:1.9`](#chronograf19)
-	[`chronograf:1.9-alpine`](#chronograf19-alpine)
-	[`chronograf:1.9.1`](#chronograf191)
-	[`chronograf:1.9.1-alpine`](#chronograf191-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.6`

```console
$ docker pull chronograf@sha256:576af240e6eadee28f5b5fc16ad0b88408d60f036cae6e222af406c096f54b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6` - linux; amd64

```console
$ docker pull chronograf@sha256:7ac2460d6aa1728bb78e0b9da1a8bc8373e73410880442e290e0df160f21f252
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49359043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875f76f03539a1b040ebf8afce7797b69893a6a9648e15377dfebbea1220064`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:55:07 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 02 Dec 2021 03:55:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:55:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:55:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:55:19 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:55:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:55:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:55:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2482d4214810296eeacf3e969c3edf369d6be0b04733fd692d04428db1dda5a8`  
		Last Modified: Thu, 02 Dec 2021 03:57:18 GMT  
		Size: 20.0 MB (20045229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e913fdab329d8f2e0e8301cd1ee94c5e7e1a236edc32cbf8706d220cf24616`  
		Last Modified: Thu, 02 Dec 2021 03:57:13 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219c22e6c2ce5ae49d1edb69990de1f14582e963ac6dab5fdd9dafe7cf9b5a25`  
		Last Modified: Thu, 02 Dec 2021 03:57:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37497e9a317e7e0ec5ea248ff0b9b143cb7d50b4977a9c699d35ee9318b13f10`  
		Last Modified: Thu, 02 Dec 2021 03:57:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0d2d4ce5d5484b9bc4087de96941128474538dcfd9b4641ce61d442861ec4a5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad44d4e11d0c8d97b32c9ea8e9c95a505d211fd6b5ec3c7892bc128883074f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:09:04 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Dec 2021 17:09:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:09:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:09:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:09:23 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:09:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:09:23 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:09:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88863c76eb7d63de7c31c7603e07e78b6e629a17f296dc9b94a9ed0eb39161f4`  
		Last Modified: Fri, 03 Dec 2021 17:12:48 GMT  
		Size: 18.8 MB (18820496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03a4b1768da3b329ad00e3af71cb254eb6cae9e395dcc2f3fa49f73029086e`  
		Last Modified: Fri, 03 Dec 2021 17:12:35 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72227ac5d42031938cedc5111c59d32c21a937b5157be08ff0645b41d826af2c`  
		Last Modified: Fri, 03 Dec 2021 17:12:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ccce34b7c6030a845affeea2c84bd0818d9e0d3ff2d10835dedb88717de639`  
		Last Modified: Fri, 03 Dec 2021 17:12:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8b9ee03e57d8477c2e7f59e55bef3e09863bdbdf1067d661cefa0a702c362685
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b932045e1cb7a511601154851d700a82ae682e7a3a95f076c4228ae8450b92b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:45:50 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 02 Dec 2021 15:45:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:45:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:46:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:46:00 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:46:01 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:46:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:46:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8dfc732c299641a36aa99b992925878206238120f9b3a7c90136afa05d8d12`  
		Last Modified: Thu, 02 Dec 2021 15:47:56 GMT  
		Size: 19.0 MB (18961228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498c82d1cd1706020ed3de481d62a038389f966301993c712c7c3423f155ca40`  
		Last Modified: Thu, 02 Dec 2021 15:47:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2824f0f4c17ce7cbe9ff8cd8df8d610e70fc255e211722c6c79e487301225b6`  
		Last Modified: Thu, 02 Dec 2021 15:47:53 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af001e89a2696c61fff58dc0baa3a912a975afe00ade091ddd49484690acae6e`  
		Last Modified: Thu, 02 Dec 2021 15:47:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6-alpine`

```console
$ docker pull chronograf@sha256:d83014d2850383073830fe3cc8b1dd10280ccadb3dc727fc46c18f0133876e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:42be608ccf5cf8a282705866e53559a2f683cee86f301d5335d2b0a8a722d1a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14867541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72592bc7b5181925382f61d3755716a15c0a3222db4caad2f764f58f7c77f70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 12 Nov 2021 21:55:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:32 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168157deaab4ba90e7cb5d2b6d5e649804bbf43d504044d8e9f3b7d8572f1935`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 11.7 MB (11738046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b8146058f9a9b104394531bbfffada3698450341aa41fa890a7a4aae65320`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36021c872f9879231ff8873fe042d102c69ef4a5a63c1b5a3fdf00ac44b9467`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09ac85e2c2a25870fabd125b2933114782d6d8dc3b752bc9c5ebfd77bb0764`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2`

```console
$ docker pull chronograf@sha256:576af240e6eadee28f5b5fc16ad0b88408d60f036cae6e222af406c096f54b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.6.2` - linux; amd64

```console
$ docker pull chronograf@sha256:7ac2460d6aa1728bb78e0b9da1a8bc8373e73410880442e290e0df160f21f252
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49359043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0875f76f03539a1b040ebf8afce7797b69893a6a9648e15377dfebbea1220064`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:55:07 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 02 Dec 2021 03:55:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:55:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:55:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:55:19 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:55:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:55:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:55:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:55:20 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2482d4214810296eeacf3e969c3edf369d6be0b04733fd692d04428db1dda5a8`  
		Last Modified: Thu, 02 Dec 2021 03:57:18 GMT  
		Size: 20.0 MB (20045229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e913fdab329d8f2e0e8301cd1ee94c5e7e1a236edc32cbf8706d220cf24616`  
		Last Modified: Thu, 02 Dec 2021 03:57:13 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219c22e6c2ce5ae49d1edb69990de1f14582e963ac6dab5fdd9dafe7cf9b5a25`  
		Last Modified: Thu, 02 Dec 2021 03:57:13 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37497e9a317e7e0ec5ea248ff0b9b143cb7d50b4977a9c699d35ee9318b13f10`  
		Last Modified: Thu, 02 Dec 2021 03:57:13 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0d2d4ce5d5484b9bc4087de96941128474538dcfd9b4641ce61d442861ec4a5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43944235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15ad44d4e11d0c8d97b32c9ea8e9c95a505d211fd6b5ec3c7892bc128883074f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:09:04 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 03 Dec 2021 17:09:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:09:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:09:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:09:23 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:09:23 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:09:23 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:09:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:09:24 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88863c76eb7d63de7c31c7603e07e78b6e629a17f296dc9b94a9ed0eb39161f4`  
		Last Modified: Fri, 03 Dec 2021 17:12:48 GMT  
		Size: 18.8 MB (18820496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b03a4b1768da3b329ad00e3af71cb254eb6cae9e395dcc2f3fa49f73029086e`  
		Last Modified: Fri, 03 Dec 2021 17:12:35 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72227ac5d42031938cedc5111c59d32c21a937b5157be08ff0645b41d826af2c`  
		Last Modified: Fri, 03 Dec 2021 17:12:35 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ccce34b7c6030a845affeea2c84bd0818d9e0d3ff2d10835dedb88717de639`  
		Last Modified: Fri, 03 Dec 2021 17:12:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.6.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8b9ee03e57d8477c2e7f59e55bef3e09863bdbdf1067d661cefa0a702c362685
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45421807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b932045e1cb7a511601154851d700a82ae682e7a3a95f076c4228ae8450b92b0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:45:50 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Thu, 02 Dec 2021 15:45:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:45:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:46:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:46:00 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:46:01 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:46:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:46:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:46:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8dfc732c299641a36aa99b992925878206238120f9b3a7c90136afa05d8d12`  
		Last Modified: Thu, 02 Dec 2021 15:47:56 GMT  
		Size: 19.0 MB (18961228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498c82d1cd1706020ed3de481d62a038389f966301993c712c7c3423f155ca40`  
		Last Modified: Thu, 02 Dec 2021 15:47:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2824f0f4c17ce7cbe9ff8cd8df8d610e70fc255e211722c6c79e487301225b6`  
		Last Modified: Thu, 02 Dec 2021 15:47:53 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af001e89a2696c61fff58dc0baa3a912a975afe00ade091ddd49484690acae6e`  
		Last Modified: Thu, 02 Dec 2021 15:47:53 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.6.2-alpine`

```console
$ docker pull chronograf@sha256:d83014d2850383073830fe3cc8b1dd10280ccadb3dc727fc46c18f0133876e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.6.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:42be608ccf5cf8a282705866e53559a2f683cee86f301d5335d2b0a8a722d1a7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.9 MB (14867541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72592bc7b5181925382f61d3755716a15c0a3222db4caad2f764f58f7c77f70b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:18 GMT
ENV CHRONOGRAF_VERSION=1.6.2
# Fri, 12 Nov 2021 21:55:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:aa4a9d01295c7013d89da92a943af071556aea6dbe6269affd4664fdd86969b8 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:32 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:32 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:32 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168157deaab4ba90e7cb5d2b6d5e649804bbf43d504044d8e9f3b7d8572f1935`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 11.7 MB (11738046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7b8146058f9a9b104394531bbfffada3698450341aa41fa890a7a4aae65320`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36021c872f9879231ff8873fe042d102c69ef4a5a63c1b5a3fdf00ac44b9467`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09ac85e2c2a25870fabd125b2933114782d6d8dc3b752bc9c5ebfd77bb0764`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:43c6e15895a192d6c520fceafc853c69de00b23042c2add545baed8ac91ec0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:c5c5aa415ab129ba3554becbc283223a012f35981518353d146a8dc3332cf003
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65388141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25401e310306453a57297b4f2de07b89f36146d379ef08cd1ff170e93fa40e95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:55:41 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 02 Dec 2021 03:55:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:55:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:55:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:55:59 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:55:59 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:55:59 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7555a1a53cfc51049bacb03b1303258e0c0f07cfae51e0d06ba50373f75ab47`  
		Last Modified: Thu, 02 Dec 2021 03:57:29 GMT  
		Size: 4.5 MB (4506609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f84e7c21c2488db7f15a38dc3083d6ca00a42434353ceea3e1f501b45f36a9d`  
		Last Modified: Thu, 02 Dec 2021 03:57:35 GMT  
		Size: 38.3 MB (38328052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810aaa0fe662e8e79257595697fee04ceaea1a7d7fe84fadbebf08cab97bc9a3`  
		Last Modified: Thu, 02 Dec 2021 03:57:28 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62cfad6394f16e20db343de9b619a351df8ae9d38511284819f0e17de043e71`  
		Last Modified: Thu, 02 Dec 2021 03:57:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f787f7cec7f5eb6ffb496ce856863729eeeba90f6c5112bebda9f0b09029b`  
		Last Modified: Thu, 02 Dec 2021 03:57:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a935e833dd6a1248792d27ed2612bd6888e248c8b1ba0f26756caad486955ac5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59006425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6072acbe56e175122e092bb0a1da76c97cce1eeeb031affc126b5ea6bf40701c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:09:54 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Dec 2021 17:10:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:10:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:10:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:10:28 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:10:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:10:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:10:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:10:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95a57db35ef7d699b9188db92b1cc0b22d04adcb3ef28f1738e83e0bd602215`  
		Last Modified: Fri, 03 Dec 2021 17:13:02 GMT  
		Size: 3.9 MB (3879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e480534410d8454f7a0f7144a81bb01d18ae2d52f050611347b799a5d3a83de`  
		Last Modified: Fri, 03 Dec 2021 17:13:19 GMT  
		Size: 35.8 MB (35783426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317efff2d37c2810422e08e8371a54b5ef0720f424a1d1209fbe77ace1225607`  
		Last Modified: Fri, 03 Dec 2021 17:13:00 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cd6e3f78dea88969d45ca30481b9e9add89f0517783c3d47ea4f8c720a31b3`  
		Last Modified: Fri, 03 Dec 2021 17:13:00 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3fd55cecf51f6389fef6a81ce5cf337849313a481ec3e59665daa1299cb53f`  
		Last Modified: Fri, 03 Dec 2021 17:13:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3f58cc41cb06810dc849adedcf749d36cf6e3763f7b7863746c5fcb51ffea490
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bea7bf5786b8ae1746804da081b493c1a52752f356a7a8c37b203b468b224b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:46:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:46:28 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 02 Dec 2021 15:46:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:46:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:46:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:46:42 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:46:43 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:46:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:46:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:46:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e204ce9347945edaa1fb2d3e97d6114f50e79b2e8c5a811f301c562d1e4a2e8`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 3.9 MB (3893777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350fc13eb93b4fa10ac5c30151ee5119bd8a9444289df4a075be21209ec19b1`  
		Last Modified: Thu, 02 Dec 2021 15:48:11 GMT  
		Size: 36.0 MB (35986778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee257abb2cffd5d3af25924c9010702c67e1b23f7c1517dc082e21fa1d4dedc7`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a79cc7ccd2ecd1f3928db18f946e12aba27dc148a132fbffe8b482bb0f606eb`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45307fd580c82f41badd472419a6f7f223986e1324d143bbf59d31c32ece36a1`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:997ecebb69bae99483291c00663c3d1d2ec0628a1c0abb4aae057cc7b004570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:77cf883ffa62d74117fd7c6e4a998199f6fbb063e654a42b8046a6cfe3ce69b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22686062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027745c7d556a42156b262cea5fa7ff78b10d534ae6c2a4decd69caaeedaa26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:38 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 12 Nov 2021 21:55:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:45 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:46 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a3b7cad208670302a759a3e65783b946b1fb9221a8ab882fef07277d38d3`  
		Last Modified: Fri, 12 Nov 2021 21:56:59 GMT  
		Size: 19.6 MB (19556570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b447bd4534f47d32c04a9937b72b986d155e25c02cb3add58d4a1c700940c3`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deac552aa1d37ccee70bddc7022a3ce80dad98b87b9fd130543f7fa787be0caa`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656207cac83a586c1a7cf9aec72e8f8cc2ee68c672d3cf8403ff18631c28cf2`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:43c6e15895a192d6c520fceafc853c69de00b23042c2add545baed8ac91ec0be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:c5c5aa415ab129ba3554becbc283223a012f35981518353d146a8dc3332cf003
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.4 MB (65388141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25401e310306453a57297b4f2de07b89f36146d379ef08cd1ff170e93fa40e95`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:55:41 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 02 Dec 2021 03:55:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:55:58 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:55:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:55:59 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:55:59 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:55:59 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7555a1a53cfc51049bacb03b1303258e0c0f07cfae51e0d06ba50373f75ab47`  
		Last Modified: Thu, 02 Dec 2021 03:57:29 GMT  
		Size: 4.5 MB (4506609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f84e7c21c2488db7f15a38dc3083d6ca00a42434353ceea3e1f501b45f36a9d`  
		Last Modified: Thu, 02 Dec 2021 03:57:35 GMT  
		Size: 38.3 MB (38328052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810aaa0fe662e8e79257595697fee04ceaea1a7d7fe84fadbebf08cab97bc9a3`  
		Last Modified: Thu, 02 Dec 2021 03:57:28 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62cfad6394f16e20db343de9b619a351df8ae9d38511284819f0e17de043e71`  
		Last Modified: Thu, 02 Dec 2021 03:57:28 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297f787f7cec7f5eb6ffb496ce856863729eeeba90f6c5112bebda9f0b09029b`  
		Last Modified: Thu, 02 Dec 2021 03:57:28 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a935e833dd6a1248792d27ed2612bd6888e248c8b1ba0f26756caad486955ac5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59006425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6072acbe56e175122e092bb0a1da76c97cce1eeeb031affc126b5ea6bf40701c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:09:54 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 03 Dec 2021 17:10:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:10:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:10:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:10:28 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:10:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:10:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:10:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:10:30 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95a57db35ef7d699b9188db92b1cc0b22d04adcb3ef28f1738e83e0bd602215`  
		Last Modified: Fri, 03 Dec 2021 17:13:02 GMT  
		Size: 3.9 MB (3879892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e480534410d8454f7a0f7144a81bb01d18ae2d52f050611347b799a5d3a83de`  
		Last Modified: Fri, 03 Dec 2021 17:13:19 GMT  
		Size: 35.8 MB (35783426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:317efff2d37c2810422e08e8371a54b5ef0720f424a1d1209fbe77ace1225607`  
		Last Modified: Fri, 03 Dec 2021 17:13:00 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cd6e3f78dea88969d45ca30481b9e9add89f0517783c3d47ea4f8c720a31b3`  
		Last Modified: Fri, 03 Dec 2021 17:13:00 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c3fd55cecf51f6389fef6a81ce5cf337849313a481ec3e59665daa1299cb53f`  
		Last Modified: Fri, 03 Dec 2021 17:13:00 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:3f58cc41cb06810dc849adedcf749d36cf6e3763f7b7863746c5fcb51ffea490
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60294310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37bea7bf5786b8ae1746804da081b493c1a52752f356a7a8c37b203b468b224b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:46:28 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gpg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:46:28 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 02 Dec 2021 15:46:40 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:46:41 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:46:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:46:42 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:46:43 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:46:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:46:45 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:46:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e204ce9347945edaa1fb2d3e97d6114f50e79b2e8c5a811f301c562d1e4a2e8`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 3.9 MB (3893777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9350fc13eb93b4fa10ac5c30151ee5119bd8a9444289df4a075be21209ec19b1`  
		Last Modified: Thu, 02 Dec 2021 15:48:11 GMT  
		Size: 36.0 MB (35986778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee257abb2cffd5d3af25924c9010702c67e1b23f7c1517dc082e21fa1d4dedc7`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a79cc7ccd2ecd1f3928db18f946e12aba27dc148a132fbffe8b482bb0f606eb`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45307fd580c82f41badd472419a6f7f223986e1324d143bbf59d31c32ece36a1`  
		Last Modified: Thu, 02 Dec 2021 15:48:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:997ecebb69bae99483291c00663c3d1d2ec0628a1c0abb4aae057cc7b004570c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:77cf883ffa62d74117fd7c6e4a998199f6fbb063e654a42b8046a6cfe3ce69b1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22686062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c027745c7d556a42156b262cea5fa7ff78b10d534ae6c2a4decd69caaeedaa26`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:38 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 12 Nov 2021 21:55:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:55:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:55:45 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:55:46 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:55:46 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:55:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:55:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8283a3b7cad208670302a759a3e65783b946b1fb9221a8ab882fef07277d38d3`  
		Last Modified: Fri, 12 Nov 2021 21:56:59 GMT  
		Size: 19.6 MB (19556570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b447bd4534f47d32c04a9937b72b986d155e25c02cb3add58d4a1c700940c3`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deac552aa1d37ccee70bddc7022a3ce80dad98b87b9fd130543f7fa787be0caa`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 11.9 KB (11895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1656207cac83a586c1a7cf9aec72e8f8cc2ee68c672d3cf8403ff18631c28cf2`  
		Last Modified: Fri, 12 Nov 2021 21:56:55 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:7065cae7169c122afbd52a08f20d8789523719187219e49feffb6755b08738c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:0ecbc28f9d3db15afbe6cfd9175eebbdec8edbb4c43398404ab2d0767aaad799
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66239899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014de89d9341034e9fd092e57555693b2d0b0d46ea793a4051fc97bd05bc74dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:56:07 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 02 Dec 2021 03:56:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:56:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:56:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:56:19 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:56:20 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:56:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0c308e068d22fe95491c0678fd2f15e2560b8a76615fb1024a338c73dfc040`  
		Last Modified: Thu, 02 Dec 2021 03:57:52 GMT  
		Size: 36.9 MB (36926081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57413fbabc2e2a4449297092054012957454dfd4e5b76f1cc1cf5d3176fc7e69`  
		Last Modified: Thu, 02 Dec 2021 03:57:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f37c94bf1f787db74729c63f04851ae5518fc2a21417d1f60d061f91917645`  
		Last Modified: Thu, 02 Dec 2021 03:57:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987e7815c8f0ff147c5d801bdac7f402a1b3eb18da11f96a80d0087480fb88a3`  
		Last Modified: Thu, 02 Dec 2021 03:57:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d604b639765476cf9ecd7981d2547935338918b4b433574a97e2660b6fea17d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59635200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c514bcbd9624fc6cb4faa6e5846351209473b760487754a1b1d1c2621901fcb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:10:46 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Dec 2021 17:11:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:11:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:11:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:11:06 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:11:07 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:11:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:11:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:11:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa93a363159ab33315535a6e66624570844c454720879bc722ea9485522adc5`  
		Last Modified: Fri, 03 Dec 2021 17:13:48 GMT  
		Size: 34.5 MB (34511461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25a8a036443beb7d9c379eddd81271edaf5bb3d1a16fb977a8a0d00c59cae30`  
		Last Modified: Fri, 03 Dec 2021 17:13:31 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e87ec6401fb7716b7a5694e163146a0ebe318483737436a999c06907cd5868`  
		Last Modified: Fri, 03 Dec 2021 17:13:31 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e491d94514da197d63f78833fd845b415c4fe9fa59108feba572edaae737823d`  
		Last Modified: Fri, 03 Dec 2021 17:13:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:aad8b19a87157977b8bf2216fb4d2e26e6ed974504b0ce8b6f4e87b3a3a3e0f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60891926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893b47c7b13e3a09ee938a72ad4f7d0eb7d95d4c75ee3fa3be030ba165350558`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:46:52 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 02 Dec 2021 15:47:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:47:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:47:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:47:02 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:47:03 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:47:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:47:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:47:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107ab1775814473465aedb937209fba6740d1c178239128aa399cadf7415ae1f`  
		Last Modified: Thu, 02 Dec 2021 15:48:27 GMT  
		Size: 34.4 MB (34431339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08606cf9f34afba69ec6af48fec8a2c97e5b9d04d08052a0ec94c9ec5208dd03`  
		Last Modified: Thu, 02 Dec 2021 15:48:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c056a586d11e9a557c7232d06bd523d70f92374cf4f0acc123639dfb4e3b1cb3`  
		Last Modified: Thu, 02 Dec 2021 15:48:23 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fcfedc91eb3bbacf9500bce20be2bb0fa8d975d2af869ed3adae964d921585`  
		Last Modified: Thu, 02 Dec 2021 15:48:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:37af8f9a75619ff9a41d61b2395fad185b1daaf94aea63c81ca013ddcc112510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4f2fdffd0f89e9d26b360b63d1a7794d2511e88417b624fa63e82aceb3ecdea5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22333670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac33f8cebe8e52e9d28a37599d6205b0aa51c9ba34cd1e2bbf18b32324fe96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:51 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 12 Nov 2021 21:56:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:01 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:01 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799e7fd8ed3ec32e09323ac48e268943b7d77fc4ed3a618a2a93ae2bef5d99d4`  
		Last Modified: Fri, 12 Nov 2021 21:57:13 GMT  
		Size: 19.2 MB (19204166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126bd6c969f1bb9e4ad0a7f6f576cf330325d804279329adc1cc66549dc44358`  
		Last Modified: Fri, 12 Nov 2021 21:57:10 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a5f10b7fe32ea10409e5fabd241935dfd702349e179ae54173d56679568d9c`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860006ae37408c8d020a52a83bc91fdb91f8aea8a67a319597dfcccb0268666f`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:7065cae7169c122afbd52a08f20d8789523719187219e49feffb6755b08738c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:0ecbc28f9d3db15afbe6cfd9175eebbdec8edbb4c43398404ab2d0767aaad799
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66239899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014de89d9341034e9fd092e57555693b2d0b0d46ea793a4051fc97bd05bc74dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:56:07 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 02 Dec 2021 03:56:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:56:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:56:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:56:19 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:56:20 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:56:20 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:20 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:21 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0c308e068d22fe95491c0678fd2f15e2560b8a76615fb1024a338c73dfc040`  
		Last Modified: Thu, 02 Dec 2021 03:57:52 GMT  
		Size: 36.9 MB (36926081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57413fbabc2e2a4449297092054012957454dfd4e5b76f1cc1cf5d3176fc7e69`  
		Last Modified: Thu, 02 Dec 2021 03:57:46 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f37c94bf1f787db74729c63f04851ae5518fc2a21417d1f60d061f91917645`  
		Last Modified: Thu, 02 Dec 2021 03:57:46 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987e7815c8f0ff147c5d801bdac7f402a1b3eb18da11f96a80d0087480fb88a3`  
		Last Modified: Thu, 02 Dec 2021 03:57:46 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d604b639765476cf9ecd7981d2547935338918b4b433574a97e2660b6fea17d5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59635200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c514bcbd9624fc6cb4faa6e5846351209473b760487754a1b1d1c2621901fcb5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:10:46 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 03 Dec 2021 17:11:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:11:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:11:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:11:06 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:11:07 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:11:07 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:11:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:11:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa93a363159ab33315535a6e66624570844c454720879bc722ea9485522adc5`  
		Last Modified: Fri, 03 Dec 2021 17:13:48 GMT  
		Size: 34.5 MB (34511461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25a8a036443beb7d9c379eddd81271edaf5bb3d1a16fb977a8a0d00c59cae30`  
		Last Modified: Fri, 03 Dec 2021 17:13:31 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e87ec6401fb7716b7a5694e163146a0ebe318483737436a999c06907cd5868`  
		Last Modified: Fri, 03 Dec 2021 17:13:31 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e491d94514da197d63f78833fd845b415c4fe9fa59108feba572edaae737823d`  
		Last Modified: Fri, 03 Dec 2021 17:13:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:aad8b19a87157977b8bf2216fb4d2e26e6ed974504b0ce8b6f4e87b3a3a3e0f6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60891926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893b47c7b13e3a09ee938a72ad4f7d0eb7d95d4c75ee3fa3be030ba165350558`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:46:52 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 02 Dec 2021 15:47:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:47:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:47:02 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:47:02 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:47:03 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:47:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:47:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:47:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107ab1775814473465aedb937209fba6740d1c178239128aa399cadf7415ae1f`  
		Last Modified: Thu, 02 Dec 2021 15:48:27 GMT  
		Size: 34.4 MB (34431339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08606cf9f34afba69ec6af48fec8a2c97e5b9d04d08052a0ec94c9ec5208dd03`  
		Last Modified: Thu, 02 Dec 2021 15:48:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c056a586d11e9a557c7232d06bd523d70f92374cf4f0acc123639dfb4e3b1cb3`  
		Last Modified: Thu, 02 Dec 2021 15:48:23 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98fcfedc91eb3bbacf9500bce20be2bb0fa8d975d2af869ed3adae964d921585`  
		Last Modified: Thu, 02 Dec 2021 15:48:22 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:37af8f9a75619ff9a41d61b2395fad185b1daaf94aea63c81ca013ddcc112510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4f2fdffd0f89e9d26b360b63d1a7794d2511e88417b624fa63e82aceb3ecdea5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.3 MB (22333670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ac33f8cebe8e52e9d28a37599d6205b0aa51c9ba34cd1e2bbf18b32324fe96`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:55:51 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 12 Nov 2021 21:56:00 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:00 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:01 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:01 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:01 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:01 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:799e7fd8ed3ec32e09323ac48e268943b7d77fc4ed3a618a2a93ae2bef5d99d4`  
		Last Modified: Fri, 12 Nov 2021 21:57:13 GMT  
		Size: 19.2 MB (19204166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126bd6c969f1bb9e4ad0a7f6f576cf330325d804279329adc1cc66549dc44358`  
		Last Modified: Fri, 12 Nov 2021 21:57:10 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a5f10b7fe32ea10409e5fabd241935dfd702349e179ae54173d56679568d9c`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860006ae37408c8d020a52a83bc91fdb91f8aea8a67a319597dfcccb0268666f`  
		Last Modified: Fri, 12 Nov 2021 21:57:09 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:bd91aec2c99aae410805298cd073605cf17dc143663bfdaee9e4fbd2109bf743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:bfae11ebcaa2800e109ad78a1a88af5b50277ae3c0221128144cb3bbd5fc00c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66882260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e5397d827b44902881f17bf6a9ed6a1afbc2985ff5166a4fa3af80b35613bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:56:27 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Thu, 02 Dec 2021 03:56:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:56:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:56:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:56:39 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:56:40 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:56:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5ed1ec307de799c2029d41d8bacb529e10d73479eca5a9dca1a3fd3da18162`  
		Last Modified: Thu, 02 Dec 2021 03:58:09 GMT  
		Size: 37.6 MB (37568445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8fe35026ddf4aaad23ee8c405b9261a13c8a719fcf029de49bd8136385ada8`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da80d378991097af18e84aba7c7faa9895e6576ee0d5e632c02968d8f818ab52`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe4a8c5ba575ca7a33bb40b92586ea6b1faeea85fb763c811ec76c13d573d7`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:efb6a47c13add28ffa5004d3acb847b52d8f07f477ce7e6ef6ceb9fb9d9d34ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60402915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb43430b777974db16f3a2722b76683b81aaea3f3abe8c87af45745a78446fc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:11:20 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 03 Dec 2021 17:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:11:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:11:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:11:41 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:11:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:11:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:11:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:11:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152fc1789800ed0f2d614a3f2adb7e34e6d2f0cdb276b8f0d9ac777fd5632f07`  
		Last Modified: Fri, 03 Dec 2021 17:14:19 GMT  
		Size: 35.3 MB (35279173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15286f24b95a205211ecb41cb3bac005e55f87addae5ab7c2f6ee7475c7f30a`  
		Last Modified: Fri, 03 Dec 2021 17:14:00 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99f4603d4f081f6cb77cd2226c11cbd12d82df27703ea1f97027f6ae48bd276`  
		Last Modified: Fri, 03 Dec 2021 17:14:01 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93bb8dd9a5b41ff772413a3bc78303f4798de906f7a1f50588874fbeeba09c6`  
		Last Modified: Fri, 03 Dec 2021 17:14:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9345e9472f34a4bf7087734c4ab74513dc70aaf0fa7ab379410bf0623974afe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9793858f56c12d4fec03a514a2f8145f2e1e29f6f8ac04a994c83dc717c2160`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:47:11 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Thu, 02 Dec 2021 15:47:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:47:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:47:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:47:22 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:47:23 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:47:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:47:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be53220e9af6d6dd754a550d7790d935c7d0246c253ad4b930f114684cc6373`  
		Last Modified: Thu, 02 Dec 2021 15:48:49 GMT  
		Size: 35.2 MB (35162838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c1f0f5b4089f54d180f0a3dcdafe51e2fb8284721e30c70aab2b64624220a`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214ec9f5826c8725ade14a8f6ded123819686601cc47de2b96bd0c38cfb0469a`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2750b350888569756bdb2876c94bb545e4ccf4d4b1eeecf0bf04ace97ac6207`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:61f1153f5cbb64d78ef85eeefcdece467687ac9f285bf2c82aa23e77298521cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f058416548a083cd4eed1795030fe2a3f175baeb3975d0d6f39b3fa35c7a12ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22790730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038b29989b30a347cc92f835d8bdbb8cf9b046a2d0e79bc93d5a6c33b044288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:56:07 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 12 Nov 2021 21:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:16 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:17 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99072c44d340c8a9fe28c4fc543e6c42b35b5d7346feeb7cbd368a2efea17527`  
		Last Modified: Fri, 12 Nov 2021 21:57:27 GMT  
		Size: 19.7 MB (19661235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423a9c662479af0c48dc95fbc8c9990e352dcf3c918dde087acdc8447421a1e`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be23b2ea4c0096063257f0b44a67f6f18296d22e5a78dc135bbf2cfa43f07e72`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75249649e859aeb1cdabcd6daf012c9ad8b86ea19843eb9c30100a835327d4be`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1`

```console
$ docker pull chronograf@sha256:bd91aec2c99aae410805298cd073605cf17dc143663bfdaee9e4fbd2109bf743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.1` - linux; amd64

```console
$ docker pull chronograf@sha256:bfae11ebcaa2800e109ad78a1a88af5b50277ae3c0221128144cb3bbd5fc00c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66882260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e5397d827b44902881f17bf6a9ed6a1afbc2985ff5166a4fa3af80b35613bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:56:27 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Thu, 02 Dec 2021 03:56:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:56:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:56:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:56:39 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:56:40 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:56:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5ed1ec307de799c2029d41d8bacb529e10d73479eca5a9dca1a3fd3da18162`  
		Last Modified: Thu, 02 Dec 2021 03:58:09 GMT  
		Size: 37.6 MB (37568445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8fe35026ddf4aaad23ee8c405b9261a13c8a719fcf029de49bd8136385ada8`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da80d378991097af18e84aba7c7faa9895e6576ee0d5e632c02968d8f818ab52`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe4a8c5ba575ca7a33bb40b92586ea6b1faeea85fb763c811ec76c13d573d7`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:efb6a47c13add28ffa5004d3acb847b52d8f07f477ce7e6ef6ceb9fb9d9d34ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60402915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb43430b777974db16f3a2722b76683b81aaea3f3abe8c87af45745a78446fc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:11:20 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 03 Dec 2021 17:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:11:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:11:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:11:41 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:11:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:11:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:11:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:11:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152fc1789800ed0f2d614a3f2adb7e34e6d2f0cdb276b8f0d9ac777fd5632f07`  
		Last Modified: Fri, 03 Dec 2021 17:14:19 GMT  
		Size: 35.3 MB (35279173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15286f24b95a205211ecb41cb3bac005e55f87addae5ab7c2f6ee7475c7f30a`  
		Last Modified: Fri, 03 Dec 2021 17:14:00 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99f4603d4f081f6cb77cd2226c11cbd12d82df27703ea1f97027f6ae48bd276`  
		Last Modified: Fri, 03 Dec 2021 17:14:01 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93bb8dd9a5b41ff772413a3bc78303f4798de906f7a1f50588874fbeeba09c6`  
		Last Modified: Fri, 03 Dec 2021 17:14:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.1` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9345e9472f34a4bf7087734c4ab74513dc70aaf0fa7ab379410bf0623974afe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9793858f56c12d4fec03a514a2f8145f2e1e29f6f8ac04a994c83dc717c2160`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:47:11 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Thu, 02 Dec 2021 15:47:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:47:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:47:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:47:22 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:47:23 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:47:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:47:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be53220e9af6d6dd754a550d7790d935c7d0246c253ad4b930f114684cc6373`  
		Last Modified: Thu, 02 Dec 2021 15:48:49 GMT  
		Size: 35.2 MB (35162838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c1f0f5b4089f54d180f0a3dcdafe51e2fb8284721e30c70aab2b64624220a`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214ec9f5826c8725ade14a8f6ded123819686601cc47de2b96bd0c38cfb0469a`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2750b350888569756bdb2876c94bb545e4ccf4d4b1eeecf0bf04ace97ac6207`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.1-alpine`

```console
$ docker pull chronograf@sha256:61f1153f5cbb64d78ef85eeefcdece467687ac9f285bf2c82aa23e77298521cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.1-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f058416548a083cd4eed1795030fe2a3f175baeb3975d0d6f39b3fa35c7a12ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22790730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038b29989b30a347cc92f835d8bdbb8cf9b046a2d0e79bc93d5a6c33b044288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:56:07 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 12 Nov 2021 21:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:16 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:17 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99072c44d340c8a9fe28c4fc543e6c42b35b5d7346feeb7cbd368a2efea17527`  
		Last Modified: Fri, 12 Nov 2021 21:57:27 GMT  
		Size: 19.7 MB (19661235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423a9c662479af0c48dc95fbc8c9990e352dcf3c918dde087acdc8447421a1e`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be23b2ea4c0096063257f0b44a67f6f18296d22e5a78dc135bbf2cfa43f07e72`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75249649e859aeb1cdabcd6daf012c9ad8b86ea19843eb9c30100a835327d4be`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:61f1153f5cbb64d78ef85eeefcdece467687ac9f285bf2c82aa23e77298521cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:f058416548a083cd4eed1795030fe2a3f175baeb3975d0d6f39b3fa35c7a12ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.8 MB (22790730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2038b29989b30a347cc92f835d8bdbb8cf9b046a2d0e79bc93d5a6c33b044288`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:55:17 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:55:18 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 12 Nov 2021 21:56:07 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 12 Nov 2021 21:56:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 12 Nov 2021 21:56:16 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 12 Nov 2021 21:56:16 GMT
EXPOSE 8888
# Fri, 12 Nov 2021 21:56:17 GMT
VOLUME [/var/lib/chronograf]
# Fri, 12 Nov 2021 21:56:17 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 12 Nov 2021 21:56:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 12 Nov 2021 21:56:17 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc79f199b43e46c5dfea12dfa8b92b7811e74b4d3812ff99c8368e4d2af803e7`  
		Last Modified: Fri, 12 Nov 2021 21:56:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aac166cdd02de2f1baf9250ebe4e1a5bec54cc49a59dbb3716570ed37d5bf63`  
		Last Modified: Fri, 12 Nov 2021 21:56:43 GMT  
		Size: 282.0 KB (281961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99072c44d340c8a9fe28c4fc543e6c42b35b5d7346feeb7cbd368a2efea17527`  
		Last Modified: Fri, 12 Nov 2021 21:57:27 GMT  
		Size: 19.7 MB (19661235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d423a9c662479af0c48dc95fbc8c9990e352dcf3c918dde087acdc8447421a1e`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 12.3 KB (12264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be23b2ea4c0096063257f0b44a67f6f18296d22e5a78dc135bbf2cfa43f07e72`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 11.9 KB (11896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75249649e859aeb1cdabcd6daf012c9ad8b86ea19843eb9c30100a835327d4be`  
		Last Modified: Fri, 12 Nov 2021 21:57:24 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:bd91aec2c99aae410805298cd073605cf17dc143663bfdaee9e4fbd2109bf743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:bfae11ebcaa2800e109ad78a1a88af5b50277ae3c0221128144cb3bbd5fc00c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66882260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e5397d827b44902881f17bf6a9ed6a1afbc2985ff5166a4fa3af80b35613bc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 02:50:30 GMT
ADD file:8177796e1ceff490318ed6eb46346bef21c5bcf01b1b396567475a1333d77174 in / 
# Thu, 02 Dec 2021 02:50:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:55:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 03:56:27 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Thu, 02 Dec 2021 03:56:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 03:56:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 03:56:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 03:56:39 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 03:56:40 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 03:56:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 03:56:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 03:56:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4f470726ddc3d7ee51215c25ddc9d02185d04304b081eb283cbeb217964b939`  
		Last Modified: Thu, 02 Dec 2021 02:57:41 GMT  
		Size: 22.5 MB (22529080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7ac851948306ff0cad2418221cb3d1b3db35a10c8d199e71d24da55c907a6`  
		Last Modified: Thu, 02 Dec 2021 03:57:15 GMT  
		Size: 6.8 MB (6760339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5ed1ec307de799c2029d41d8bacb529e10d73479eca5a9dca1a3fd3da18162`  
		Last Modified: Thu, 02 Dec 2021 03:58:09 GMT  
		Size: 37.6 MB (37568445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c8fe35026ddf4aaad23ee8c405b9261a13c8a719fcf029de49bd8136385ada8`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da80d378991097af18e84aba7c7faa9895e6576ee0d5e632c02968d8f818ab52`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe4a8c5ba575ca7a33bb40b92586ea6b1faeea85fb763c811ec76c13d573d7`  
		Last Modified: Thu, 02 Dec 2021 03:58:03 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:efb6a47c13add28ffa5004d3acb847b52d8f07f477ce7e6ef6ceb9fb9d9d34ab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60402915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb43430b777974db16f3a2722b76683b81aaea3f3abe8c87af45745a78446fc7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 09:11:13 GMT
ADD file:07a27489332bd5ff2b73df3ba5210164fa947c12b65e248d0449d7fd69c6b760 in / 
# Thu, 02 Dec 2021 09:11:14 GMT
CMD ["bash"]
# Fri, 03 Dec 2021 17:09:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 03 Dec 2021 17:11:20 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Fri, 03 Dec 2021 17:11:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 03 Dec 2021 17:11:40 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 03 Dec 2021 17:11:40 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 03 Dec 2021 17:11:41 GMT
EXPOSE 8888
# Fri, 03 Dec 2021 17:11:41 GMT
VOLUME [/var/lib/chronograf]
# Fri, 03 Dec 2021 17:11:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 03 Dec 2021 17:11:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 03 Dec 2021 17:11:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d264feab9f2b883bc5096deb677e485d44e353381c2e9c571053bf54514ca9a6`  
		Last Modified: Thu, 02 Dec 2021 09:28:31 GMT  
		Size: 19.3 MB (19318707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ef3409b253375b66ef6bbd8a1731da1f8f803b2cd035477ab54909cb9cff9d`  
		Last Modified: Fri, 03 Dec 2021 17:12:38 GMT  
		Size: 5.8 MB (5780631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152fc1789800ed0f2d614a3f2adb7e34e6d2f0cdb276b8f0d9ac777fd5632f07`  
		Last Modified: Fri, 03 Dec 2021 17:14:19 GMT  
		Size: 35.3 MB (35279173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e15286f24b95a205211ecb41cb3bac005e55f87addae5ab7c2f6ee7475c7f30a`  
		Last Modified: Fri, 03 Dec 2021 17:14:00 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99f4603d4f081f6cb77cd2226c11cbd12d82df27703ea1f97027f6ae48bd276`  
		Last Modified: Fri, 03 Dec 2021 17:14:01 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93bb8dd9a5b41ff772413a3bc78303f4798de906f7a1f50588874fbeeba09c6`  
		Last Modified: Fri, 03 Dec 2021 17:14:01 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:9345e9472f34a4bf7087734c4ab74513dc70aaf0fa7ab379410bf0623974afe8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.6 MB (61623426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9793858f56c12d4fec03a514a2f8145f2e1e29f6f8ac04a994c83dc717c2160`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 02 Dec 2021 08:10:23 GMT
ADD file:d9d01d3468e590cea0e2803b24fa9d34ca1d3eb31b517a5a0edf081f85e7dcc1 in / 
# Thu, 02 Dec 2021 08:10:23 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 15:45:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 02 Dec 2021 15:47:11 GMT
ENV CHRONOGRAF_VERSION=1.9.1
# Thu, 02 Dec 2021 15:47:19 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 02 Dec 2021 15:47:21 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 02 Dec 2021 15:47:22 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 02 Dec 2021 15:47:22 GMT
EXPOSE 8888
# Thu, 02 Dec 2021 15:47:23 GMT
VOLUME [/var/lib/chronograf]
# Thu, 02 Dec 2021 15:47:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 02 Dec 2021 15:47:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 02 Dec 2021 15:47:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:99dcd33b7a52fa23a15c1dc3456487807f7ad0f48f3df675dc13490656cc96f9`  
		Last Modified: Thu, 02 Dec 2021 08:44:55 GMT  
		Size: 20.4 MB (20389365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9835a9e5e5d57344917a5fabf910eaf75af9ec080f69195c4fe8e6abca11cac`  
		Last Modified: Thu, 02 Dec 2021 15:47:54 GMT  
		Size: 6.0 MB (6046823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be53220e9af6d6dd754a550d7790d935c7d0246c253ad4b930f114684cc6373`  
		Last Modified: Thu, 02 Dec 2021 15:48:49 GMT  
		Size: 35.2 MB (35162838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61c1f0f5b4089f54d180f0a3dcdafe51e2fb8284721e30c70aab2b64624220a`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214ec9f5826c8725ade14a8f6ded123819686601cc47de2b96bd0c38cfb0469a`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2750b350888569756bdb2876c94bb545e4ccf4d4b1eeecf0bf04ace97ac6207`  
		Last Modified: Thu, 02 Dec 2021 15:48:44 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
