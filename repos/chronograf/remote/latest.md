## `chronograf:latest`

```console
$ docker pull chronograf@sha256:07cba7b069e5ec7027d942b35a250358052174485c704f58aec1e2b4a7c3dcb9
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
$ docker pull chronograf@sha256:a5d5997fa575a11cbbd441528193b5078fea3221b6a6e5ea87598d4b28d1f0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.6 MB (84581820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ecc21483ba8601581e9fde57391810fae4e11a9b6ca8f29c89c96ec401cfc0f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd5f7720f7246dde5561426d82d564eda3f7d36bb3a6670a3770bc88134d9db7`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 7.9 MB (7875466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d937045b0d245509e6a15651490c28bbcf2ba34649a5e898a032e7b7b395fd30`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 48.5 MB (48454620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3ba974b6bb30cd12c43de5fc77a036818922515181202f95eb483d1a4d9b99`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb68d523da02175326435a308d4bda88e8185209a42f58bca62a8cb6b20fc266`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aab054931a65ce6eb03aaaea053ef5dc76ffde78efca071816c4fb4dcb34f499`  
		Last Modified: Tue, 08 Apr 2025 01:24:50 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:cd5a67855a871f08b9ea1c7c594e0ac0792e7ec64559b320cff680508cae2a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:417c68170030f6ab0af55006508c3683fa3c6877eafa4678e99ef3c5cca621f8`

```dockerfile
```

-	Layers:
	-	`sha256:37053d94ba4f693d609b03ba15afb047eba84e57a85b148edc7b53982509d434`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 2.7 MB (2704173 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a42a5cfa2b45c3d1c2e3a99db05f5fc6af7686c6c1a560928658d4207fdbf213`  
		Last Modified: Tue, 08 Apr 2025 01:24:49 GMT  
		Size: 16.1 KB (16128 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:079db0bd2d86f924708a5a9e6de6c2cb7d3399cf1699f557229137991509ac54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75344233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a5aa6b6d812c629928d618bac6db5743606f7239a3a3a26aaad9013d7807ef`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a4cae4b4be11b615ad8d998f77262f16fb70375bec9f1790dc5e05cce9a5d4`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 6.5 MB (6497876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ca6161fddf786d8012dd22432d04af6253ee18bf5410e706918e4de84897a3`  
		Last Modified: Tue, 08 Apr 2025 07:41:53 GMT  
		Size: 44.9 MB (44884033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6d2e2d402730b3e47c70c7a8aabe0d0793ccf8eb0697f589f07e8d11c841be`  
		Last Modified: Tue, 08 Apr 2025 07:41:51 GMT  
		Size: 12.2 KB (12242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791bbc1f7129cabc57b97efda40df8c58cc17296f8496c736de68e6aa6067c61`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8db94257bbf594cc0bd3f1146569a9345620758022b6acfc42d15cd2507084`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:9739812ff99a5b6697d386b42a97788bd24f1863f33aa2b651293d38893bb3fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a8caa4b6b0ca8884ce0cbd8e9fa634519d744fe87bd92a071278e921b8e34a`

```dockerfile
```

-	Layers:
	-	`sha256:7d9aabb618915996af35c9036eff103c458b5b41627180a237317e736eb873da`  
		Last Modified: Tue, 08 Apr 2025 07:41:52 GMT  
		Size: 2.7 MB (2706470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21f063817b819d3672d30970228e48a1f0fe85493751bb5fac5cd4df2f4cd441`  
		Last Modified: Tue, 08 Apr 2025 07:41:51 GMT  
		Size: 16.2 KB (16209 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8d09faba86fbf271e53e98a9284de3d8208ce87338cf0859550d19201f57e982
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.0 MB (82026956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1af4d2e6e170d6540fc4cf36fa34596f75e1266535d408024ebdfc38b6498d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 17 Dec 2024 14:20:15 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Tue, 17 Dec 2024 14:20:15 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENV CHRONOGRAF_VERSION=1.10.6
# Tue, 17 Dec 2024 14:20:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 17 Dec 2024 14:20:15 GMT
VOLUME [/var/lib/chronograf]
# Tue, 17 Dec 2024 14:20:15 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 17 Dec 2024 14:20:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 17 Dec 2024 14:20:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6bdd77a3e8191d60b227c9f755f6f8f4b05034647007a07c82c1f6e4e88fd5`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 7.7 MB (7652075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8259506abfecb0d9cefbd5da4e67b42720a246f8ee84521a7debe53fd757ba9`  
		Last Modified: Tue, 08 Apr 2025 06:06:41 GMT  
		Size: 46.3 MB (46284096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b303ae82d885113e78bb9e74c59a3e208975cc6de99b17cdda23c65c431f17cf`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d00ef9f739ada971c5ff08863c9ae4b2a5dd0fb640b56931da3efe57697831`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8236a193f0c09a8aa82a0a8535f11cd23a4896d4e7607979e84f340192e25fa4`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:89e855ac93e95ac2c414f1c7ba3731319ed22a82629cdb1a16686f71650629b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaffee6edec55303d2718b0134fe372c5e802220e816f225534996bcc0d9d0b4`

```dockerfile
```

-	Layers:
	-	`sha256:53bb146925fab3e7f4222f9293b00b8f7b9a918a381581d8818f36045f7b13b4`  
		Last Modified: Tue, 08 Apr 2025 06:06:40 GMT  
		Size: 2.7 MB (2704446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:390ca5bb55650e1e1291992921fd0e2cad9783ef561abcb28b2d5e1c9dde57a5`  
		Last Modified: Tue, 08 Apr 2025 06:06:39 GMT  
		Size: 16.2 KB (16235 bytes)  
		MIME: application/vnd.in-toto+json
