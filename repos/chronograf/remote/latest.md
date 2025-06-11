## `chronograf:latest`

```console
$ docker pull chronograf@sha256:10ad064ee4e5ac24d6042e0405959490fdf8041233fc89094a5f590c148c054e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:3fa34988b249b4444e84238bdde42974a493793b661995e94a0f91969568dbb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.4 MB (85366212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e0678a7ac88e0b02c4319eb24bead15691f7e855f4eacbebbd61a1640b397a2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d910ca1dbe966e093bbe1995f852aa86741793aabdffd4c61660dc381b7fa69`  
		Last Modified: Tue, 10 Jun 2025 23:37:31 GMT  
		Size: 7.9 MB (7877923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db6221c517a305d2515a1185a984bb9221b8878f86e194f154fe0bcb314f68c4`  
		Last Modified: Tue, 10 Jun 2025 23:37:36 GMT  
		Size: 49.2 MB (49233694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799dfdfaa99f1e72c2d31de3259c7135e62b54f80d0dafb4b2b764438622557e`  
		Last Modified: Tue, 10 Jun 2025 23:37:31 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dac435ae2705c415f72ebbae96828c8d65719ba96bc2ab21b36c6b0b195523f`  
		Last Modified: Tue, 10 Jun 2025 23:37:31 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77121a24ce8abde41771324b327754ba8b4dcbb5b5ff22ef306720430d4243a`  
		Last Modified: Tue, 10 Jun 2025 23:37:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:e627333a053ad7f5f3c424539c299d1fd2c084ccdc6f0b3de0a4f1e6688fa728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb74cbdbdf45a5bb80e54ae2eb52906fe3f2885b0ba2d53ab9a68331923600d6`

```dockerfile
```

-	Layers:
	-	`sha256:c7399b02cec970d60ecf206ffa84bada73637e8dc5740ea889e324e99139591b`  
		Last Modified: Wed, 11 Jun 2025 00:38:19 GMT  
		Size: 2.9 MB (2850477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aed4e8e4fa6075b2717c2b0fd273e57be7775ae68e42cea13a95754cf67e655`  
		Last Modified: Wed, 11 Jun 2025 00:38:20 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6008d2538bce61f67a1ae2712589b4f67057528e8f759d2db90410345b6f25de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76024093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095cfdb2794ec2d5bf62af461d1ca38272b0a47183671d1954304291bc969e4a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360bf5dc02a13e8fbde9f96cd089523ec5cf245313b8a6443c2ab1455d5e4b0f`  
		Last Modified: Tue, 03 Jun 2025 17:35:17 GMT  
		Size: 6.5 MB (6502016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2522014972f589023e7a6ee691cf90c3b8e394860f55a4ca663af8dd18f15d2`  
		Last Modified: Tue, 03 Jun 2025 17:35:21 GMT  
		Size: 45.6 MB (45564688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734772e99c21723f959350d5ab539b5fa07e977f3c550783dc2685807e52e0ea`  
		Last Modified: Tue, 03 Jun 2025 17:35:18 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439b762429d0d3d33150b45b7819b117c7691890cb28fb9358a0ec230bde5594`  
		Last Modified: Tue, 03 Jun 2025 17:35:19 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3fbd2efb705976268c34d6e6945bb4fbda57e3e47ca2dee8217f8384449012e`  
		Last Modified: Tue, 03 Jun 2025 17:35:20 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ddfbb500d334f80c0d47a7a830ba9087bfbc17c1af79901d506659053d6b52d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2747764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fac8183e69cf83b21c35411c716f7429a543b18ca7c21c17a4b84c1a00b119c8`

```dockerfile
```

-	Layers:
	-	`sha256:9b273eff8befe6f28782d0299078353f943703085c2ff035c8173b9e10ecf8bb`  
		Last Modified: Wed, 04 Jun 2025 19:01:41 GMT  
		Size: 2.7 MB (2731555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a5c2a3474fb8c424c70892a37094b95c0014b49a0860fee64f2ffcb04cf64a6`  
		Last Modified: Wed, 04 Jun 2025 19:01:43 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:13d44ecd31f78d26c120b24910927bc329f792510c5677fb21a69250a8a20916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82764391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476d31c6094f77885a3c60c694bd0f2a20075f00aee21e18805fe5d79bfc74e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 16 Apr 2025 11:55:02 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENV CHRONOGRAF_VERSION=1.10.7
# Wed, 16 Apr 2025 11:55:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 16 Apr 2025 11:55:02 GMT
VOLUME [/var/lib/chronograf]
# Wed, 16 Apr 2025 11:55:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Apr 2025 11:55:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Apr 2025 11:55:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbf62f4d51f539fa5656951e43e5ffbd4a7b81beccfa677ee5cef24fff0dac0`  
		Last Modified: Tue, 03 Jun 2025 14:29:32 GMT  
		Size: 7.7 MB (7654129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b461db01c536574d304d6f0d8e3a54a5da4ab36660ee0d555cea5c57b49f3c`  
		Last Modified: Tue, 03 Jun 2025 14:29:34 GMT  
		Size: 47.0 MB (47020519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abcf7dfea80c70db56d88d755cd13252971a733cd15a6e8d5e017b51c9971b59`  
		Last Modified: Tue, 03 Jun 2025 14:29:31 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf266ff177054f437ddee6d0727fa94c7c5142721504fbc34111bb123afbc5d`  
		Last Modified: Tue, 03 Jun 2025 14:29:33 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b90c830635b3530d1836d5e6a650a5c116aa7df795677277a68eeb6f31bf4228`  
		Last Modified: Tue, 03 Jun 2025 14:29:34 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:8b8be9d9826add0b1c6781ed5cdc79f51c287b7eaa3ba07597f4a01b2d0f3ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2745765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa07a2ffe7dc0de3644e9b10e97775307fd06c1d1137fb528916c09655245b4`

```dockerfile
```

-	Layers:
	-	`sha256:5ceed79ad3b60067bb91524aa025ce5db26e1bd88ad06cb9fe8a5589d40ad9bc`  
		Last Modified: Wed, 04 Jun 2025 19:02:22 GMT  
		Size: 2.7 MB (2729531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:846462090e3d46c0e6fb7e0229d1c3ef587589500b1e671ea1f233992c847b81`  
		Last Modified: Wed, 04 Jun 2025 19:02:25 GMT  
		Size: 16.2 KB (16234 bytes)  
		MIME: application/vnd.in-toto+json
