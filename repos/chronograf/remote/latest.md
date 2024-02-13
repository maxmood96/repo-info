## `chronograf:latest`

```console
$ docker pull chronograf@sha256:c169697b69fdb23ee6689fbf5d94815bfb9bed0cf4b733a2f66960bd4cbf23dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:04462ac26b7dbe7a416cce7de3b7cb3f980b2902a3b0ea0945b2b48574b8c61d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84071849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba864730ae6dd40df4e4518818953064d84a262247c361f41dd3c4696b995db`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:37:22 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
# Tue, 13 Feb 2024 00:37:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:37:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:37:30 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:37:37 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:37:37 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:37:37 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:37:37 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:37:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:37:38 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4699424b1273b826b5cdc341e3b641e4677c94540188c99dbfe6107f04b338`  
		Last Modified: Tue, 13 Feb 2024 01:38:40 GMT  
		Size: 7.9 MB (7870359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdf86bc6e62c35c39e6459d906c2630014debc2e98d324647a464bbebf11e69`  
		Last Modified: Tue, 13 Feb 2024 01:38:45 GMT  
		Size: 47.1 MB (47053015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212a2b45925a777bacea28fb46859ff3c9d814027aa8c86354e32ff87ea2909`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2998c8c8e76f333407adb69b20a7daf0d2eda63ff22da8b98eb2e40f0ace65d`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a23ee363789d93f633ec5fd788469b8fd511b4832198e334f0cf1a4ea393a1b`  
		Last Modified: Tue, 13 Feb 2024 01:38:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:5a8f81b92103e745298e8c422bc2da762d61f221b133678c2665b19ddcffd63a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75914249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e46ec2f2c9b6df884dcef26780f2d0aeb6fda789fd804792eba274adbc31e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:20 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
# Wed, 31 Jan 2024 22:44:20 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:14:39 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 31 Jan 2024 23:14:39 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Wed, 31 Jan 2024 23:14:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Wed, 31 Jan 2024 23:14:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Wed, 31 Jan 2024 23:14:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Wed, 31 Jan 2024 23:14:52 GMT
EXPOSE 8888
# Wed, 31 Jan 2024 23:14:52 GMT
VOLUME [/var/lib/chronograf]
# Wed, 31 Jan 2024 23:14:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Wed, 31 Jan 2024 23:14:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 31 Jan 2024 23:14:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4746837155da551ba7b85a6dbb7317ac9724fafed36183e0432ed2786348d3fc`  
		Last Modified: Wed, 31 Jan 2024 23:15:49 GMT  
		Size: 6.5 MB (6497856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a2d442c7129d2daa164171c07090055d600430504e4c7ff1685ab0585128b57`  
		Last Modified: Wed, 31 Jan 2024 23:15:52 GMT  
		Size: 44.7 MB (44650431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6092283a9646dad6a647c45a5e30f2f14fe9a4807502cbde74299634a70cc4`  
		Last Modified: Wed, 31 Jan 2024 23:15:45 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff8d4185e0f15429811c21fd79ef6dffd387a5fdb9bca711d0b2c7026275f4ec`  
		Last Modified: Wed, 31 Jan 2024 23:15:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd590a155ec653e117cff3112914ff6adac1cfdcc39fec8e0e27fc201b35905`  
		Last Modified: Wed, 31 Jan 2024 23:15:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5d8d80646010cfe6875f70f0305283c4ecf410af01669a7739bbb99f6ab4d71c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ea9755b59d1150652ef5cf7cf8d8fcb4e8d418288516d3ba6d9b18a3a00b5b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 13 Feb 2024 00:41:20 GMT
ADD file:a3e4f94158c3515dc70de5aa81c136a9f7daf5adcac636a15c237097cb454140 in / 
# Tue, 13 Feb 2024 00:41:20 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:52:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 13 Feb 2024 01:52:22 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 13 Feb 2024 01:52:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 13 Feb 2024 01:52:28 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 13 Feb 2024 01:52:28 GMT
EXPOSE 8888
# Tue, 13 Feb 2024 01:52:29 GMT
VOLUME [/var/lib/chronograf]
# Tue, 13 Feb 2024 01:52:29 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 13 Feb 2024 01:52:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Feb 2024 01:52:29 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f546e941f15b76df3d982d56985432b05bc065e3923fb35be25a4d33d5c0f911`  
		Last Modified: Tue, 13 Feb 2024 00:44:54 GMT  
		Size: 29.2 MB (29156363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8356d255d957337b3271ca2ccb409831d13fb862aa8674a62d51e2a0cf121c5`  
		Last Modified: Tue, 13 Feb 2024 01:53:15 GMT  
		Size: 7.6 MB (7647144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae248ef7539fbb6f443297ba9bd3c53a1fc193086a6befe57cf3165c6eee1f5`  
		Last Modified: Tue, 13 Feb 2024 01:53:19 GMT  
		Size: 44.8 MB (44773513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b1b3905f9f2f89ae89d40f805eaaffd9b634c0bdbd3e9dfdb75ae53737a4bb`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0252bd3162130e739e5cabd7d9e9bea09a6b3ef32210f0103dbd7be761759e0d`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7a271221e0ffe0f48af65b288d14a19ab326cfcf5088ab1fda68f49415702c`  
		Last Modified: Tue, 13 Feb 2024 01:53:14 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
