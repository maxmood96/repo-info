## `chronograf:latest`

```console
$ docker pull chronograf@sha256:2746b239ff4be0efc6f402b1aeb5fe431fbe7abe3b0d73dd9d30ad4a2f4e1ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:5e147cd584cc40d42a9ac5ad8b05892dd7def2826e426050d12b33f4e206288c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81235348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181ca155af9072dff68e616f46ffeb6a6e86d08036194c0d3b67ca015392d45d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:32 GMT
ADD file:73e68ae6852c9afbb2989dc9c5b7c6668843f454b1bdcfb48658bfbc6c4af69e in / 
# Wed, 21 Dec 2022 01:20:33 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 01:47:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 21 Dec 2022 01:47:47 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Wed, 21 Dec 2022 01:47:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 21 Dec 2022 01:47:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 21 Dec 2022 01:47:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 21 Dec 2022 01:47:55 GMT
EXPOSE 8888
# Wed, 21 Dec 2022 01:47:55 GMT
VOLUME [/var/lib/chronograf]
# Wed, 21 Dec 2022 01:47:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 21 Dec 2022 01:47:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 21 Dec 2022 01:47:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f4ca61aafcd4fc07267a105067db35c0f0ac630e1970f3cd0c7bf552780e985`  
		Last Modified: Wed, 21 Dec 2022 01:24:36 GMT  
		Size: 31.4 MB (31396943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42710022201b4041517538b3a692f1ae88a0ec8c9646567df3d05bf9b09a37`  
		Last Modified: Wed, 21 Dec 2022 01:48:36 GMT  
		Size: 5.2 MB (5226800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43185987e07d673338ff668e3ec4ad0ae414aa8764ccc819daa46e2a3b791fbd`  
		Last Modified: Wed, 21 Dec 2022 01:49:11 GMT  
		Size: 44.6 MB (44587208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451016ff8a51b54246c631725ac73043d0487c20425abb51151962ad40964c49`  
		Last Modified: Wed, 21 Dec 2022 01:49:05 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c18610532b58e3f5a781742491c6d8d3183edbe842846cd69379ee856d3b3`  
		Last Modified: Wed, 21 Dec 2022 01:49:05 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c806cb526b4dbab7dc6d1b7cc633047bce85ee9a0622fd73bfead331185c27b4`  
		Last Modified: Wed, 21 Dec 2022 01:49:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:940df312875251e09bb551952c88e719e921217382ca2c0e458d679581d0206b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73560703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46c8e5d166b1c72df66ec7e56027579e92b228d2e13fff21043839e020152f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 00:58:51 GMT
ADD file:cb354f875d5631d5d4542ab57d0b9b323a261f5c631d5917127504d6eb54d85a in / 
# Tue, 06 Dec 2022 00:58:52 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 10:15:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 10:16:29 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 10:16:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 10:16:38 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 10:16:38 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 10:16:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 10:16:39 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 10:16:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 10:16:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4f32a98d14d26603bb8e8cf9bda992e24606d2fe00101767049a01d5176929e1`  
		Last Modified: Tue, 06 Dec 2022 01:06:05 GMT  
		Size: 26.6 MB (26576348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13331aa96eaee2e9e3ef374955946cbe0508467ec66e9c44cb3122bc85393b6e`  
		Last Modified: Tue, 06 Dec 2022 10:17:29 GMT  
		Size: 4.5 MB (4495026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b493b2a2579f2080785c4a4e7d3db8e4d7e25e6e0afce8a048cafd3b0c0cfb`  
		Last Modified: Tue, 06 Dec 2022 10:18:08 GMT  
		Size: 42.5 MB (42464936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8875c67483f82bc20ddf506d0b3f57cac5bdc74b4ff8c31caf40a6b3b8931597`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1458f13cd06ea42cd5ae8d1d467c93cf83f290077dad0887a29a5b3f74a87596`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31c35ed9bc20a5bb6678297d9f268738785c2af7b2a63949d0ad2e4dd873b310`  
		Last Modified: Tue, 06 Dec 2022 10:18:00 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:b9a923a7f9577ea18562ca96d20f9092d3564d8b7fdbab907678a2125762c73d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.9 MB (77914187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b562de4f793f8bfe522fb78778dadf5df254c69bff24023d08eda93fbfe602`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:17 GMT
ADD file:379d6ac56afdb6e02d71fa0faebc13b8a2554fc6ae76c5f5bbdb5b8e475135d6 in / 
# Tue, 06 Dec 2022 01:40:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:15:19 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 06 Dec 2022 02:15:36 GMT
ENV CHRONOGRAF_VERSION=1.10.0
# Tue, 06 Dec 2022 02:15:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 06 Dec 2022 02:15:42 GMT
EXPOSE 8888
# Tue, 06 Dec 2022 02:15:42 GMT
VOLUME [/var/lib/chronograf]
# Tue, 06 Dec 2022 02:15:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 06 Dec 2022 02:15:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 06 Dec 2022 02:15:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6064e7e5b6afa4dc711228eddfd250aebac271830dc184c400ce640020bc2cb0`  
		Last Modified: Tue, 06 Dec 2022 01:43:56 GMT  
		Size: 30.1 MB (30060320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010bcfd47e4f0331c64dfb2af5573bf99a4b88b4d972387850c61ff6ef0d11a9`  
		Last Modified: Tue, 06 Dec 2022 02:16:10 GMT  
		Size: 5.2 MB (5211566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63cfceb30c24c808b43865619c58241102c036bd153c354e2f2f1457954400`  
		Last Modified: Tue, 06 Dec 2022 02:16:37 GMT  
		Size: 42.6 MB (42617907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb34459112efb5b29d1c5cbe97dad350e283c8259b45e077aa3104ff0a7c432b`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21072e41358457fcdb1399f31b7dd73322af50a96fc66fe37b8841d39bb92579`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca77523a925a0d9872b733837dba904a8a82c95de486d5f95f5bf8678deb165`  
		Last Modified: Tue, 06 Dec 2022 02:16:32 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
