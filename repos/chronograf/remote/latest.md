## `chronograf:latest`

```console
$ docker pull chronograf@sha256:a56b0f0904455b0ba92c3c9eb1957a7712aff1322b74a71d29a8b240c3174f94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:0424fae67c92415d422ca244a4935fb0455907c365debe6272ff9488c5e328de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66240585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b7178f5b2768f98cf4e87e5dbf7c9bf03cb71ee4665941270562d4fe4adf423`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 00:47:17 GMT
ADD file:55a25b93e8f2940a796f3cbf1e78bddf5f49c46b1b89b63b9b5673cbed9483ca in / 
# Thu, 22 Jul 2021 00:47:17 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:19:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:20:41 GMT
ENV CHRONOGRAF_VERSION=1.8.9
# Tue, 10 Aug 2021 23:20:49 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:20:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:20:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:20:50 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:20:50 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:20:50 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:20:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:20:51 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:778066204fb734c2fb80cb8127cb35d67d742806a4eaf1aba0b5393c4ae6f2a4`  
		Last Modified: Thu, 22 Jul 2021 00:53:22 GMT  
		Size: 22.5 MB (22527428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6a7366e2bde34bd805efd550017364593938f57a4a46acc844edd839bb011c`  
		Last Modified: Tue, 10 Aug 2021 23:21:24 GMT  
		Size: 6.8 MB (6760080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52cfe543ac77c073d25e490187403f12e6a2ddd9a28cfa39e2bfdc7e3cc856f`  
		Last Modified: Tue, 10 Aug 2021 23:22:22 GMT  
		Size: 36.9 MB (36928698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0875f5f8188a212f1e0ecbbea8b681c37fda177e2d077e825f661a1887cd3d`  
		Last Modified: Tue, 10 Aug 2021 23:22:17 GMT  
		Size: 12.2 KB (12241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab263271f31dcd063f19e670d7660db9039bd3d3c0fabb414dd7d8a61c3f6e7b`  
		Last Modified: Tue, 10 Aug 2021 23:22:18 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47cdf755ad75192ab1b3abdb470cfe23e267884f7386c7c5d86f2aa45c5d548c`  
		Last Modified: Tue, 10 Aug 2021 23:22:17 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:aaa12f3421fbcc2da74abf990ee7e7515ef96f85710f3361d890a52991d3d8d7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.6 MB (59617640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065f7eaeabb6ce83c6ac6cb1cfe4e40568460463aa8b45664a6797fbec021dee`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 02:07:27 GMT
ADD file:86bd875241ca751f2f50a9c3504cfca4ce772411fed23fe6893299a271c275e3 in / 
# Thu, 22 Jul 2021 02:07:28 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:00:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:02:02 GMT
ENV CHRONOGRAF_VERSION=1.8.9
# Tue, 10 Aug 2021 23:02:21 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:02:22 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:02:23 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:02:23 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:02:24 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:02:24 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:02:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:02:25 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:37325b08023150a9e16c0c8d98d10daa998ce21ec3b9226cc6f0148a245a8a57`  
		Last Modified: Thu, 22 Jul 2021 02:21:16 GMT  
		Size: 19.3 MB (19315955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84236a4145013894eb753d54367ba39e700f41448379d11fb8acf79e2100e630`  
		Last Modified: Tue, 10 Aug 2021 23:03:14 GMT  
		Size: 5.8 MB (5779562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563aa1050ffeff783f5c0ace0c0d4c26bf42c55be8a64652b976ba2242844480`  
		Last Modified: Tue, 10 Aug 2021 23:04:29 GMT  
		Size: 34.5 MB (34497735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33390c7d3a170ef269b4e0664ab92012f5e8a0be393ea68452543bc3805dd86`  
		Last Modified: Tue, 10 Aug 2021 23:04:10 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63513570675210dbda0283a576386daa6c1305131230de9124c5a42c5b9ede1`  
		Last Modified: Tue, 10 Aug 2021 23:04:11 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001f573921c3e4fda4891864bdc68ad985bbec2316df915bf5b962fb9cc9cced`  
		Last Modified: Tue, 10 Aug 2021 23:04:10 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:a5f40bdcb37c74441a63f07860475d9ddf91a14e4f447e247def81645f4c915f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60874986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:079690ec080f4cc51cae064179be41397c302fea0de396f47440c49b59b88aac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 22 Jul 2021 00:41:40 GMT
ADD file:b39a01b3af7a531df3592571b7f6eaa7efd20919858f7f0cd2ddf1c1eceb078d in / 
# Thu, 22 Jul 2021 00:41:40 GMT
CMD ["bash"]
# Tue, 10 Aug 2021 23:39:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 10 Aug 2021 23:40:22 GMT
ENV CHRONOGRAF_VERSION=1.8.9
# Tue, 10 Aug 2021 23:40:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 10 Aug 2021 23:40:30 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 10 Aug 2021 23:40:30 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 10 Aug 2021 23:40:30 GMT
EXPOSE 8888
# Tue, 10 Aug 2021 23:40:31 GMT
VOLUME [/var/lib/chronograf]
# Tue, 10 Aug 2021 23:40:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 10 Aug 2021 23:40:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 10 Aug 2021 23:40:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:9e7a560784c85cb9624bff5b6e479fbb95d5e265873987014f8aec75d509a530`  
		Last Modified: Thu, 22 Jul 2021 00:48:50 GMT  
		Size: 20.4 MB (20389427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2662c6178e07a9035450aa3ce2945f23d2b96f3ff9c97fb90010d16b89e412`  
		Last Modified: Tue, 10 Aug 2021 23:40:54 GMT  
		Size: 6.0 MB (6047457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e04db06e129561598bc9a656554e9838dd0d4800c2093f4635c81374ab0b62`  
		Last Modified: Tue, 10 Aug 2021 23:41:30 GMT  
		Size: 34.4 MB (34413711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f31c64e323f50e1b9f9232c2ef49d3b6cdfad958f22cd80acf6ac0c95f8df4c`  
		Last Modified: Tue, 10 Aug 2021 23:41:25 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf247884ce4c6ef0357eacc30b3d6115b18a430d4eec49c84a0f6415be4fb62`  
		Last Modified: Tue, 10 Aug 2021 23:41:25 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6029ddd9e6d47d64d29297032e05f6eb50749eebb20b09fe77c90339406d9eb`  
		Last Modified: Tue, 10 Aug 2021 23:41:25 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
