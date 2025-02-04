## `chronograf:latest`

```console
$ docker pull chronograf@sha256:122648e92ca72280daf200b61f3c86a4b008e216645a1833a198883d3aadaf52
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
$ docker pull chronograf@sha256:5c778bc81892bf7d857e84056d7f404c08d8e1a8b3a61b8be78c3456444e6c3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.3 MB (83329784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc6296f978c36c764aeba47abfda2c2f8cfb6b6d335e6613447702b2671f9dc`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea4677274335b6d13e9d85d2cb59ce3c040ab4fe297a219c71486d0a997fdf60`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 7.9 MB (7875460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e341bdf0db524398c580141c359facb380260a87e863fd011ab4f9fd9f18700`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 47.2 MB (47217554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b773fd7294d9043bd106a1bd32e4ae5d935c95fa2f6c71e8402c967af36daa`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959c37d0b325d913afc6820bc08751b8c345ececd2e9019a6eebe37bbbef5fed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b22ab05d59f0f8196b08ac45a7b94f98c851c519e6c70a6c1c99113ca2fb67ed`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:1b2e6e5404f443d80444bddcc3f103f3b8f87280e6912fae9f228d314a7877d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2719989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7461f550112f8d4354117a9c1ef0e0bc7ece095b4991a5f14e7ae843b83643c`

```dockerfile
```

-	Layers:
	-	`sha256:4d2610d19117b875074759f759521347e466a19de34b8e92d9f6758c8f854b06`  
		Last Modified: Tue, 04 Feb 2025 04:38:20 GMT  
		Size: 2.7 MB (2703861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c59690fa3689bb8814d4273ccbf864c2d4cb427966be0444f656eb830c15c81`  
		Last Modified: Tue, 04 Feb 2025 04:38:19 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b8eaf491a3d51ab1ad081116051d6319665ea6a159f15552fb042a8880452e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74713234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1631585b9c6c1e93b600a77695687e7dd10bb578920dd6f3c03efc21143d4f7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1736726400'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f7fde15b664589586a61b714ca6b43dec045d0f187d81d4eb050918e17b0ff1e`  
		Last Modified: Tue, 14 Jan 2025 01:35:15 GMT  
		Size: 23.9 MB (23914600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31eb12efed5eb5b137542a8591ffaddcfec2ab7fbb3e4d81891c4d2ddc47283c`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 6.5 MB (6497830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff49de7a4cba1c7f1e033fadd98d847bc9f2aed1a1b8faac5681a4d17c5590ec`  
		Last Modified: Tue, 14 Jan 2025 09:02:48 GMT  
		Size: 44.3 MB (44276343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c409b1b91c6fc27ad30d021a65179e77d13efde84ee96abf30a124f3a86825`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d49e53e707da3ed5d73b62a4fe374bad1d91274ce451a98133353442723fb9`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639c7cd00071a0b62766d53b22370535830272a699de91971e54d828c113c6c2`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:cb2388b11815c41e02b9ed158ee6d627b8e7e9ba4baae043731552a2ce9f769e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07c2b25ff90a5be47dfbfe81063611749d333225960cec7a16874dd2006fd37`

```dockerfile
```

-	Layers:
	-	`sha256:e00d8906b7526bc8bca4dbd34a2d75af98b178ba57c9dc6badeb508556ff8f5f`  
		Last Modified: Tue, 14 Jan 2025 09:02:47 GMT  
		Size: 2.7 MB (2706158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:309aae5baec8f6e76452e0ee1b5f805d2e41571eee241086ef065f31862b2e51`  
		Last Modified: Tue, 14 Jan 2025 09:02:46 GMT  
		Size: 16.2 KB (16208 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:53bf600637ff3534af5ba40d4f62f1f62bf265e88f62746bff0720b1f27581ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80687924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e5e820a7be219fb37b71b917f93d93a8cfc1396ed76bbcfbef459a6f2c8aecb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 03 Jun 2024 14:32:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Mon, 03 Jun 2024 14:32:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENV CHRONOGRAF_VERSION=1.10.5
# Mon, 03 Jun 2024 14:32:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
EXPOSE map[8888/tcp:{}]
# Mon, 03 Jun 2024 14:32:31 GMT
VOLUME [/var/lib/chronograf]
# Mon, 03 Jun 2024 14:32:31 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Mon, 03 Jun 2024 14:32:31 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 03 Jun 2024 14:32:31 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a2a96500e7bd79e08a636c2dd8de64aaf81c75eb26ca72e5592e04ef3a0bfa`  
		Last Modified: Tue, 04 Feb 2025 09:05:18 GMT  
		Size: 7.7 MB (7652073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93621aa9b0185f06521ecd22d7b6067e6c8d3f61198c065ef75f2e6c5893e3e1`  
		Last Modified: Tue, 04 Feb 2025 09:05:19 GMT  
		Size: 45.0 MB (44970507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0b1dde535819f9761dfc7969e6b4a3442d28ff4d3783e43d5a677f8670503f`  
		Last Modified: Tue, 04 Feb 2025 09:05:18 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb0eda398c1acfae54e96a9c8f4fca309de8d0dfbf9905f7f3f2d9bfda53556`  
		Last Modified: Tue, 04 Feb 2025 09:05:18 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49cda142cdcd02ba501fcd17398db08e42c0942df88252aae4f2ae3fb0c3472`  
		Last Modified: Tue, 04 Feb 2025 09:05:19 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:6291563a4eea5059f94906c4758ddc49ba80f56cc094ff717a6c13eb581f3c39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcb7631247f1f57be8a9b7bc4a8bfaf18219379fe8845b9a739ccd234dc5e31f`

```dockerfile
```

-	Layers:
	-	`sha256:c39d94004da1552886f42869b6f4255e6bdaf22eac4790f4fd592c827c0ae891`  
		Last Modified: Tue, 04 Feb 2025 09:05:18 GMT  
		Size: 2.7 MB (2704134 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:188bad6b35cf5bd5f224cbda633215852cb1a68cd69848afa9544f21d5fe9ca6`  
		Last Modified: Tue, 04 Feb 2025 09:05:18 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
