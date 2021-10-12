## `chronograf:latest`

```console
$ docker pull chronograf@sha256:98a22af2a7be35d3ec859197856c13446eee0fa2aedce32e604a66b71d923a6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:aaea951b5f320fe4e7d041fe9ec9d49dbd521f05537caefe1cb31eab793c5ea9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66757613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05070621bd7952dad5f4565a7466f2ed27514d2fad47646e1c2bec97313ece70`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:22:52 GMT
ADD file:1220579e31585dec45ca8e35874eb689018ed026a1f23b7906f791c0279671e0 in / 
# Tue, 12 Oct 2021 01:22:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:13:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 15:14:36 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 15:14:44 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 15:14:44 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 15:14:45 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 15:14:45 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 15:14:45 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 15:14:45 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 15:14:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 15:14:46 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:eec53b8a5053c739b5b685cb372b38eea3286ab6626532bad963291f76357c5f`  
		Last Modified: Tue, 12 Oct 2021 01:29:50 GMT  
		Size: 22.5 MB (22527572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9af087790cf4907eb60360fae75759db60331cfdfb749ae8593e374a3afb328f`  
		Last Modified: Tue, 12 Oct 2021 15:15:15 GMT  
		Size: 6.8 MB (6760208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428f39960a7f8d0006300a974ae86a69f8187f11e8598ab7917a8393b5498cbd`  
		Last Modified: Tue, 12 Oct 2021 15:16:05 GMT  
		Size: 37.4 MB (37445441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4725bf7e4c46d8c7e159ad0a2891e0fddfa77e31151155e909a15eef1bb8c316`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2b58092a3477c6240ae4a362c9639d501b9e384bfa3654246d9ebcee892123`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f71aad39dc5739f7a9e2f382448e46d433ea77813f54f08d637ccc536eeb6a5`  
		Last Modified: Tue, 12 Oct 2021 15:16:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1eaf9d54e80ec37220bf2e5c6772857401e611fa6e2974575ea238562e5eca8b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60286017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3a0ed0ab3e2cf3af8f6c357383296fab4fc5a676f0dec7a7c3a9d6241605f3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Sep 2021 18:09:32 GMT
ADD file:a037f8ced10b72f1e0d62328b77376ea1efe206b6116e858b7a641d26fd5b1b0 in / 
# Thu, 30 Sep 2021 18:09:33 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 05:16:44 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 01 Oct 2021 05:19:09 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Fri, 01 Oct 2021 05:19:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Oct 2021 05:19:29 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Oct 2021 05:19:30 GMT
EXPOSE 8888
# Fri, 01 Oct 2021 05:19:30 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Oct 2021 05:19:31 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Fri, 01 Oct 2021 05:19:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Oct 2021 05:19:32 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fce8291cdcf067da304d19441e493cb62fd5be1dcc768569fdeb1e0db374c983`  
		Last Modified: Thu, 30 Sep 2021 18:26:53 GMT  
		Size: 19.3 MB (19316455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746784bfad62d65116943e0e010a50702ae1fb03d897851e36ad6b7b9fb15f4f`  
		Last Modified: Fri, 01 Oct 2021 05:20:27 GMT  
		Size: 5.8 MB (5780591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f70d7dadcc587b01abb272b80cd64ba42d1e0d123c14ba94201cee1546f599f`  
		Last Modified: Fri, 01 Oct 2021 05:22:08 GMT  
		Size: 35.2 MB (35164577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e81f2620fb3a78dd449c871aa0dffb8d612270c0e4926e70bd9a4ac20d22872`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76af3bdd08d13774a02d1879f55bd572d8fef6cce9f936f0a5457bd76d04986`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf79df797875a5efea73a0584f057cd1ec273b5e125195997c57e405c247186`  
		Last Modified: Fri, 01 Oct 2021 05:21:50 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:f8b10eabd6a93f7fcbc8d8acce2b60e412754a07bb95664a8b3caa800ca21c38
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.5 MB (61523317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc16a9b86e7c3cd6838f8aae38c005ab4d37fd1595c576151580683e74909a5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 12 Oct 2021 01:43:29 GMT
ADD file:ebfc214a3da7b706f0759fd22fa991c905976d2c970b2d59d134753f7cbd5e06 in / 
# Tue, 12 Oct 2021 01:43:29 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:24:49 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 12 Oct 2021 02:25:45 GMT
ENV CHRONOGRAF_VERSION=1.9.0
# Tue, 12 Oct 2021 02:25:52 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 12 Oct 2021 02:25:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 12 Oct 2021 02:25:53 GMT
EXPOSE 8888
# Tue, 12 Oct 2021 02:25:53 GMT
VOLUME [/var/lib/chronograf]
# Tue, 12 Oct 2021 02:25:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 12 Oct 2021 02:25:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 12 Oct 2021 02:25:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0b0a22641ad2aad782c696887c59bf05ec0b1e7aa1e07902ee51949bab802657`  
		Last Modified: Tue, 12 Oct 2021 01:52:33 GMT  
		Size: 20.4 MB (20389450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e693941dd06bd7505ff4633db32f85f682bb43790f889c3700a0cc8f95a8775a`  
		Last Modified: Tue, 12 Oct 2021 02:26:22 GMT  
		Size: 6.0 MB (6047991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc03711acce0b5e2f3e2ad7249ce4962fdd520835a1c778de663b9f2bec5f309`  
		Last Modified: Tue, 12 Oct 2021 02:27:14 GMT  
		Size: 35.1 MB (35061492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ac3e7452691d4edc39f45e7e6706d3dcf06f188bb81aa96749fe12906f31bc`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef8988907a0a7be1f7d83a61d1aeaf02ef140108fff7f975c89339dd03e7848`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9b5f2079e26ff03ed792915e6a981d31ea534399c82cf9eee4a529a07ae60`  
		Last Modified: Tue, 12 Oct 2021 02:27:09 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
