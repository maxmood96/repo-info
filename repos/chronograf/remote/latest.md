## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1afddbf9d6a54d90a34a53e598a6aa97d7fa79c7c18587b2b38a86c04c00a1d5
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
$ docker pull chronograf@sha256:255aba612f27699d8671b299b68ff18c6f80899632ca495ee82a8e50222d2107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76029846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9cdd81752909f0451b427e7fb9077321b2c0edfafbbc206312a884512fad878`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
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
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b67169da7e567ef8b872e84812501e5a0919588452e1b6bc869e0a1f90b6d2`  
		Last Modified: Wed, 11 Jun 2025 07:20:27 GMT  
		Size: 6.5 MB (6501949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f90c624c11a5b2fd2f0446b05ad51cbcbdcc260f0f381f06c0613880236175`  
		Last Modified: Wed, 11 Jun 2025 07:20:32 GMT  
		Size: 45.6 MB (45564683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f5c939f7f555f9427ea1b241f70eba9b7e2259ea945fe357d2a6c3ffe1e737`  
		Last Modified: Wed, 11 Jun 2025 05:12:26 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaff33866078d70b21af40eb2d38584fe5eaa7fb85dc8ba31db99dcd85c0dbd`  
		Last Modified: Wed, 11 Jun 2025 05:12:30 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc881d3aa9816e333446fecb24a53dd8c174535d47208e79fc5ab0f6392ac96d`  
		Last Modified: Wed, 11 Jun 2025 05:12:36 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:ad7617c9bfce8d96791b62625574c65a5cef2a72ba1b957847faff094a47a8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2868983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8007fee4768ba769bc6ea016e79fe5c853502282705d5fa10e076c0584eeea`

```dockerfile
```

-	Layers:
	-	`sha256:a9fed9299aaaba67d732f588c3641017cf0be89ff47ad6fa933a7f2893e2aac2`  
		Last Modified: Wed, 11 Jun 2025 06:38:22 GMT  
		Size: 2.9 MB (2852774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fa9a5a409568fadd2b8e118a74db759bdd6a618dcda412fc495f70261d88a23`  
		Last Modified: Wed, 11 Jun 2025 06:38:23 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:fa9ff3fa57af460f38f8e892efe013862e9abaf46abdc5ce6b1d326788ec73cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82776860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f91cf9091379c4f68d026f6a826db4d8917ea40fa6f79ba6ec73a14359f2a68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 16 Apr 2025 11:55:02 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9a2d8b510e17266ac78c42703e012e13cdeb397417670c22b62c98db03a380`  
		Last Modified: Wed, 11 Jun 2025 02:59:28 GMT  
		Size: 7.7 MB (7654166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e61a6efdb19198ab588ef967a409622a51ce1060cf49331e704a901f044ceb0`  
		Last Modified: Wed, 11 Jun 2025 02:59:35 GMT  
		Size: 47.0 MB (47020548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e46032b75f867b6d699ccac59a9d66680194c86d32c8312f4dcdeb944d2ce4`  
		Last Modified: Wed, 11 Jun 2025 02:59:28 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a42ba1c40168dd768a2891b1004b9e84b2fbf0963fa3d5f9955d158e24fbdf`  
		Last Modified: Wed, 11 Jun 2025 02:59:28 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab97c8199f5bf40742bfeb53e72b628592d5b80fb17665f5f7ca853ee865fb2`  
		Last Modified: Wed, 11 Jun 2025 02:59:28 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:a57ef9e0f92cf8c85a707480732d1d52b74f183fafc0c7d1a744769b23061bef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2866985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df50259e23919741a747c05c02b8c6f6c5aa201d3290ad246f7c615cbbad7a1`

```dockerfile
```

-	Layers:
	-	`sha256:b235c9c0aca0f529b675f8d26f77cf8c3db6aeab24ffd8b5fabd00df01d85e2c`  
		Last Modified: Wed, 11 Jun 2025 03:38:27 GMT  
		Size: 2.9 MB (2850750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb32135c07df43fd8fa1e5f667dfc547158f3cf34da77434dd9269b147c12ad0`  
		Last Modified: Wed, 11 Jun 2025 03:38:28 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
