<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.2`](#chronograf1102)
-	[`chronograf:1.10.2-alpine`](#chronograf1102-alpine)
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
-	[`chronograf:1.9.4`](#chronograf194)
-	[`chronograf:1.9.4-alpine`](#chronograf194-alpine)
-	[`chronograf:alpine`](#chronografalpine)
-	[`chronograf:latest`](#chronograflatest)

## `chronograf:1.10`

```console
$ docker pull chronograf@sha256:1564fb1891f23f9d03a7e24adbc1cf788295c855cf3a0dbf65ac5e8a484bcec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:8a36118ae02c06a5523732169ff5a97976c5abde96792f9e2cc8f1ffacce0b46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84073337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0df62239302e1f6ecb647e8fbb91eda4cc29c02c59ba0006ebcb558742769d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:33:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:33:10 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Thu, 11 Jan 2024 04:33:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:33:18 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:33:18 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:33:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:33:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46513bb8447bc150084803d26f4c182db6258f58f1b1d4a5119879af7f055b54`  
		Last Modified: Thu, 11 Jan 2024 04:34:17 GMT  
		Size: 7.9 MB (7870172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de2094287552144254685d6024bfab813dbf44032b509244630b93a75be4645`  
		Last Modified: Thu, 11 Jan 2024 04:34:21 GMT  
		Size: 47.1 MB (47052856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0381ea74b82acae59b5c3208bbc176f7ba607263be258559c93d973cebac476b`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b80052a70e74ab35a78203e3c82aef19cde6e5f546af67b9a97d3db5532849`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91091f4813580d8b81a77240fcd055cef92638d713a87feda438abd423ef2039`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d003628994751531936cf990737f67d86023ce8dcb419fc6658aec7d2081c3e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75886321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3179d715357eba52a0692348fc22ddf7983cb0de165fa731480ecbe037184533`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:38:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:38:20 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Thu, 11 Jan 2024 03:38:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:38:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:38:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:38:36 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:38:36 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:38:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:38:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f7b9ecca0085cc54af13c89b81377d3f0b360a495fbf4d1aeaa85076c65f6`  
		Last Modified: Thu, 11 Jan 2024 03:39:38 GMT  
		Size: 6.5 MB (6494872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b1a6b2eaabab5ddb9bfb8f5f5a1c9bed36593aaa8561f40af782a013e350ce`  
		Last Modified: Thu, 11 Jan 2024 03:39:46 GMT  
		Size: 44.6 MB (44648935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19204c8b94fc7b4f9bc463de009cef206f893950e6608d636aa2b7b4ef8ab4`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656346136ac769804ddc702b5a0cd72eb1d229031c58751d1ddca083917653a5`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eadb16209259b77314b7dffab85374c70bd5cc8a6ff9b73c2d8b9e989f1b42`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5bd8a314f132697c0738b1448068b4e5ef4b90ec4526dc4250ad1cf1bf40d8ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2029fcba43958022c38bd47cf756be831228b0de5808b033f6352a846f37882`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:52:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:52:12 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 19 Dec 2023 06:52:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:52:19 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:52:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:52:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:52:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25528e50586e703a8d0b96794925dffd49a3c11ed5b28c7900efd2da177a3974`  
		Last Modified: Tue, 19 Dec 2023 06:53:06 GMT  
		Size: 7.6 MB (7646993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a25f7fddb0c4726b93b4c41f070fa5e979b9c974025e21868cdfbafb8f3ea7`  
		Last Modified: Tue, 19 Dec 2023 06:53:09 GMT  
		Size: 44.8 MB (44772890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b645f60a59e0181445966b8f3291ed3823c834e51bdfc1c7ed5e5d9a587272`  
		Last Modified: Tue, 19 Dec 2023 06:53:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4746b4753b6df55eaf2ee32ac0882d4766ac6baa3259568c72ff5566a942a6`  
		Last Modified: Tue, 19 Dec 2023 06:53:05 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab7e4479d3d188fc282ce7a406d2e216f222fe1f17ea23c496cbe6730249f78`  
		Last Modified: Tue, 19 Dec 2023 06:53:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:88a8f3c11c35918ccc4a79107520e7f94b36f71b4272af23f0e2bac83946079b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d6106695cafa72d587ab758ad5ea255d1a107f703cdebb5716e25070668b6cbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31559386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9f8d7783b4d1c122bc59b5d25e257c5c705b48e80425b1ca30c9b862f62e66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:36:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:36:21 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Fri, 01 Dec 2023 06:36:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:27 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822880f5cd7c4ada55339070e05a9bbdebfa8ffe320d8e04ef9484a76cce73b1`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 284.7 KB (284691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3f1f8f312b84a559d6c230bd8b16e0bc3c2fa9b0d8b5f82500f63f436f293e`  
		Last Modified: Fri, 01 Dec 2023 06:37:24 GMT  
		Size: 27.8 MB (27847590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9203360be51e26b6712f778d3e1d01a81b99f995a63bb39ac3fcfaee792a4d`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa6d5fb571ce4e663b4dcb70d144cd0146fa42d8f0b9eb984e9351607ff065`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4266056d57960899ab7424d6866e7b2ba4e13e493e9f7beb955eebcbac4d907`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2`

```console
$ docker pull chronograf@sha256:1564fb1891f23f9d03a7e24adbc1cf788295c855cf3a0dbf65ac5e8a484bcec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.2` - linux; amd64

```console
$ docker pull chronograf@sha256:8a36118ae02c06a5523732169ff5a97976c5abde96792f9e2cc8f1ffacce0b46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84073337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0df62239302e1f6ecb647e8fbb91eda4cc29c02c59ba0006ebcb558742769d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:33:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:33:10 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Thu, 11 Jan 2024 04:33:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:33:18 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:33:18 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:33:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:33:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46513bb8447bc150084803d26f4c182db6258f58f1b1d4a5119879af7f055b54`  
		Last Modified: Thu, 11 Jan 2024 04:34:17 GMT  
		Size: 7.9 MB (7870172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de2094287552144254685d6024bfab813dbf44032b509244630b93a75be4645`  
		Last Modified: Thu, 11 Jan 2024 04:34:21 GMT  
		Size: 47.1 MB (47052856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0381ea74b82acae59b5c3208bbc176f7ba607263be258559c93d973cebac476b`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b80052a70e74ab35a78203e3c82aef19cde6e5f546af67b9a97d3db5532849`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91091f4813580d8b81a77240fcd055cef92638d713a87feda438abd423ef2039`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d003628994751531936cf990737f67d86023ce8dcb419fc6658aec7d2081c3e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75886321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3179d715357eba52a0692348fc22ddf7983cb0de165fa731480ecbe037184533`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:38:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:38:20 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Thu, 11 Jan 2024 03:38:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:38:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:38:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:38:36 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:38:36 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:38:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:38:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f7b9ecca0085cc54af13c89b81377d3f0b360a495fbf4d1aeaa85076c65f6`  
		Last Modified: Thu, 11 Jan 2024 03:39:38 GMT  
		Size: 6.5 MB (6494872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b1a6b2eaabab5ddb9bfb8f5f5a1c9bed36593aaa8561f40af782a013e350ce`  
		Last Modified: Thu, 11 Jan 2024 03:39:46 GMT  
		Size: 44.6 MB (44648935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19204c8b94fc7b4f9bc463de009cef206f893950e6608d636aa2b7b4ef8ab4`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656346136ac769804ddc702b5a0cd72eb1d229031c58751d1ddca083917653a5`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eadb16209259b77314b7dffab85374c70bd5cc8a6ff9b73c2d8b9e989f1b42`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.2` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5bd8a314f132697c0738b1448068b4e5ef4b90ec4526dc4250ad1cf1bf40d8ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2029fcba43958022c38bd47cf756be831228b0de5808b033f6352a846f37882`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:52:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:52:12 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 19 Dec 2023 06:52:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:52:19 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:52:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:52:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:52:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25528e50586e703a8d0b96794925dffd49a3c11ed5b28c7900efd2da177a3974`  
		Last Modified: Tue, 19 Dec 2023 06:53:06 GMT  
		Size: 7.6 MB (7646993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a25f7fddb0c4726b93b4c41f070fa5e979b9c974025e21868cdfbafb8f3ea7`  
		Last Modified: Tue, 19 Dec 2023 06:53:09 GMT  
		Size: 44.8 MB (44772890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b645f60a59e0181445966b8f3291ed3823c834e51bdfc1c7ed5e5d9a587272`  
		Last Modified: Tue, 19 Dec 2023 06:53:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4746b4753b6df55eaf2ee32ac0882d4766ac6baa3259568c72ff5566a942a6`  
		Last Modified: Tue, 19 Dec 2023 06:53:05 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab7e4479d3d188fc282ce7a406d2e216f222fe1f17ea23c496cbe6730249f78`  
		Last Modified: Tue, 19 Dec 2023 06:53:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.2-alpine`

```console
$ docker pull chronograf@sha256:88a8f3c11c35918ccc4a79107520e7f94b36f71b4272af23f0e2bac83946079b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.2-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d6106695cafa72d587ab758ad5ea255d1a107f703cdebb5716e25070668b6cbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31559386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9f8d7783b4d1c122bc59b5d25e257c5c705b48e80425b1ca30c9b862f62e66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:36:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:36:21 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Fri, 01 Dec 2023 06:36:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:27 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822880f5cd7c4ada55339070e05a9bbdebfa8ffe320d8e04ef9484a76cce73b1`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 284.7 KB (284691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3f1f8f312b84a559d6c230bd8b16e0bc3c2fa9b0d8b5f82500f63f436f293e`  
		Last Modified: Fri, 01 Dec 2023 06:37:24 GMT  
		Size: 27.8 MB (27847590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9203360be51e26b6712f778d3e1d01a81b99f995a63bb39ac3fcfaee792a4d`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa6d5fb571ce4e663b4dcb70d144cd0146fa42d8f0b9eb984e9351607ff065`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4266056d57960899ab7424d6866e7b2ba4e13e493e9f7beb955eebcbac4d907`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:240e70f8c2a4fcaeed4f6ae042d3a2a9b120a3c7b5c720a713dc72bc4885936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:d243f36bfa49e344b72683f8e016937a5e960bdce73b443853fbdb01e25e03e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70599667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e63b396c175780c2c276191549570784a692b24893e23bddb968e4d68c782f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:32:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:32:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 11 Jan 2024 04:32:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:32:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:32:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:32:17 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:32:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:32:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:32:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:32:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49135bc4a012ef18c72f903b61ef282e923bc072f8b97ace6e9e8e18e724e1d6`  
		Last Modified: Thu, 11 Jan 2024 04:33:37 GMT  
		Size: 4.4 MB (4417356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe8fe375188ed0cbe54d905b2423fa933841ba34e0e9c55a1695eaf237e25ed`  
		Last Modified: Thu, 11 Jan 2024 04:33:40 GMT  
		Size: 34.7 MB (34739965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3886798f5fb0118c5ee57f14e35c9a1753dfad3eb6c7ca201597f7a90e237d34`  
		Last Modified: Thu, 11 Jan 2024 04:33:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c8432f8bd1ddb0380c724b791887ff2981025468930ad1a9e09705c2903df7`  
		Last Modified: Thu, 11 Jan 2024 04:33:36 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9daed096960efd3f1fcb7b7ea0c3ba8b94966edce3fd5fc253a4c69e8f2530`  
		Last Modified: Thu, 11 Jan 2024 04:33:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1f9e1c57b3a694cd4005969e2f78667c7e7435a80a868b50e143a309a024c49d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63423119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef42b72cd064b77783ef058ac36946ce641a80d5daf0c3223d03e7eb0f17c10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:36:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:36:33 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 11 Jan 2024 03:36:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:36:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:36:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:36:54 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:36:54 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:36:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:36:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:36:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad4f8b40ff033e9c95b8b79d7b1ddd203259c463c841db1ff0f139ebed1a918`  
		Last Modified: Thu, 11 Jan 2024 03:38:52 GMT  
		Size: 3.7 MB (3719978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a6e97f9a531097dc4f31fdc4921865457ca5dfa424b1c9bdd4b9bf3a3c6332`  
		Last Modified: Thu, 11 Jan 2024 03:38:57 GMT  
		Size: 33.1 MB (33099783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c50e5412c03cfa9d8911ccb0cf4beaea468ac5cb8721e8facda80a59ef56987`  
		Last Modified: Thu, 11 Jan 2024 03:38:52 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef429dadba89fbe162073e5578035c43b3484c2525bca4b0a1b223268c599fc`  
		Last Modified: Thu, 11 Jan 2024 03:38:51 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b5afe9fd3749c1fb7995469023e202b41b0639b8e9a3f5644c39ed85eb911`  
		Last Modified: Thu, 11 Jan 2024 03:38:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2b40b2c95760398a07efcb925ae90e49f8a213fbd4d6c40293eb95b771b3f63b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67747558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf58e0aca7ebfa7ee868a16f6eac40588fbd5fea39d69113bf2f731d9847bb5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:51:29 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 19 Dec 2023 06:51:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:51:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:51:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:51:36 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:51:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:51:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:51:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdedbb31db24524f68db84d95929292cc7e9d55412e64389b0d02b457f12481`  
		Last Modified: Tue, 19 Dec 2023 06:52:32 GMT  
		Size: 4.4 MB (4418967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fe5b512375d38c9b29c3861ef7501c0cad2c18192074f7d393cef0236c4624`  
		Last Modified: Tue, 19 Dec 2023 06:52:34 GMT  
		Size: 33.2 MB (33240137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e535c2729d7d3d07514af315eef49bb7323f671f7cc9e34679edb8f18057f7`  
		Last Modified: Tue, 19 Dec 2023 06:52:31 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d8fc5a62d57d75a6a844411144ffca90fce956a5f53c2b77bb2ba736cafa6e`  
		Last Modified: Tue, 19 Dec 2023 06:52:31 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b459d228b7ad51f2e07973b0f14db88a604a0caf7685a9947d7d8189a4e0be4`  
		Last Modified: Tue, 19 Dec 2023 06:52:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:23ee6556972f1e9015c5cc4e4e87c3ac035f7fa29d6c85a7f955ceb481054275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4de9c52ada973edeecf1dde9df653c357e4d751dc5c2ba5100b55fce33ecd6ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d70a911b674148c0548e26abdae870661a6d462b787149fb088ece74c74faa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:35:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:35:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 01 Dec 2023 06:35:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:35:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:35:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:35:52 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:35:52 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:35:52 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:35:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:35:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b6362e68ff3f80ca0f4dfc4b18ec97abba97d0095553e5de9a503854d2629`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 284.9 KB (284927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad218039e17cb70ca3321449b1cb765c16026568e810be13f7f24051b02317f`  
		Last Modified: Fri, 01 Dec 2023 06:36:45 GMT  
		Size: 19.6 MB (19557195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a356010b90eed0ee1414e38c7d5598fd047660a9fc67fc578d108b61dbc4b17`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 12.3 KB (12270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df3fa7eaedaf6bea10153d3fc3781d821a163d341e8f19e5be8586d545ad89e`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26922604f711fbe11e4deec648f3e7a17a0ba6fb6f0214ff86e77ee65f107d`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:240e70f8c2a4fcaeed4f6ae042d3a2a9b120a3c7b5c720a713dc72bc4885936f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:d243f36bfa49e344b72683f8e016937a5e960bdce73b443853fbdb01e25e03e8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70599667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2e63b396c175780c2c276191549570784a692b24893e23bddb968e4d68c782f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:32:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:32:08 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 11 Jan 2024 04:32:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:32:17 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:32:17 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:32:17 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:32:17 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:32:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:32:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:32:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49135bc4a012ef18c72f903b61ef282e923bc072f8b97ace6e9e8e18e724e1d6`  
		Last Modified: Thu, 11 Jan 2024 04:33:37 GMT  
		Size: 4.4 MB (4417356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe8fe375188ed0cbe54d905b2423fa933841ba34e0e9c55a1695eaf237e25ed`  
		Last Modified: Thu, 11 Jan 2024 04:33:40 GMT  
		Size: 34.7 MB (34739965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3886798f5fb0118c5ee57f14e35c9a1753dfad3eb6c7ca201597f7a90e237d34`  
		Last Modified: Thu, 11 Jan 2024 04:33:36 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c8432f8bd1ddb0380c724b791887ff2981025468930ad1a9e09705c2903df7`  
		Last Modified: Thu, 11 Jan 2024 04:33:36 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9daed096960efd3f1fcb7b7ea0c3ba8b94966edce3fd5fc253a4c69e8f2530`  
		Last Modified: Thu, 11 Jan 2024 04:33:36 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:1f9e1c57b3a694cd4005969e2f78667c7e7435a80a868b50e143a309a024c49d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63423119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef42b72cd064b77783ef058ac36946ce641a80d5daf0c3223d03e7eb0f17c10`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:36:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:36:33 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 11 Jan 2024 03:36:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:36:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:36:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:36:54 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:36:54 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:36:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:36:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:36:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad4f8b40ff033e9c95b8b79d7b1ddd203259c463c841db1ff0f139ebed1a918`  
		Last Modified: Thu, 11 Jan 2024 03:38:52 GMT  
		Size: 3.7 MB (3719978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a6e97f9a531097dc4f31fdc4921865457ca5dfa424b1c9bdd4b9bf3a3c6332`  
		Last Modified: Thu, 11 Jan 2024 03:38:57 GMT  
		Size: 33.1 MB (33099783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c50e5412c03cfa9d8911ccb0cf4beaea468ac5cb8721e8facda80a59ef56987`  
		Last Modified: Thu, 11 Jan 2024 03:38:52 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef429dadba89fbe162073e5578035c43b3484c2525bca4b0a1b223268c599fc`  
		Last Modified: Thu, 11 Jan 2024 03:38:51 GMT  
		Size: 11.9 KB (11901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:533b5afe9fd3749c1fb7995469023e202b41b0639b8e9a3f5644c39ed85eb911`  
		Last Modified: Thu, 11 Jan 2024 03:38:52 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:2b40b2c95760398a07efcb925ae90e49f8a213fbd4d6c40293eb95b771b3f63b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67747558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf58e0aca7ebfa7ee868a16f6eac40588fbd5fea39d69113bf2f731d9847bb5e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:29 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:51:29 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Tue, 19 Dec 2023 06:51:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:51:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:51:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:51:36 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:51:36 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:51:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:51:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:51:36 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fdedbb31db24524f68db84d95929292cc7e9d55412e64389b0d02b457f12481`  
		Last Modified: Tue, 19 Dec 2023 06:52:32 GMT  
		Size: 4.4 MB (4418967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fe5b512375d38c9b29c3861ef7501c0cad2c18192074f7d393cef0236c4624`  
		Last Modified: Tue, 19 Dec 2023 06:52:34 GMT  
		Size: 33.2 MB (33240137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e535c2729d7d3d07514af315eef49bb7323f671f7cc9e34679edb8f18057f7`  
		Last Modified: Tue, 19 Dec 2023 06:52:31 GMT  
		Size: 12.3 KB (12251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d8fc5a62d57d75a6a844411144ffca90fce956a5f53c2b77bb2ba736cafa6e`  
		Last Modified: Tue, 19 Dec 2023 06:52:31 GMT  
		Size: 11.9 KB (11911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b459d228b7ad51f2e07973b0f14db88a604a0caf7685a9947d7d8189a4e0be4`  
		Last Modified: Tue, 19 Dec 2023 06:52:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:23ee6556972f1e9015c5cc4e4e87c3ac035f7fa29d6c85a7f955ceb481054275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:4de9c52ada973edeecf1dde9df653c357e4d751dc5c2ba5100b55fce33ecd6ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23246128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5d70a911b674148c0548e26abdae870661a6d462b787149fb088ece74c74faa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:35:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:35:47 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Fri, 01 Dec 2023 06:35:52 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:35:52 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:35:52 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:35:52 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:35:52 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:35:52 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:35:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:35:53 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b6362e68ff3f80ca0f4dfc4b18ec97abba97d0095553e5de9a503854d2629`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 284.9 KB (284927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ad218039e17cb70ca3321449b1cb765c16026568e810be13f7f24051b02317f`  
		Last Modified: Fri, 01 Dec 2023 06:36:45 GMT  
		Size: 19.6 MB (19557195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a356010b90eed0ee1414e38c7d5598fd047660a9fc67fc578d108b61dbc4b17`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 12.3 KB (12270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df3fa7eaedaf6bea10153d3fc3781d821a163d341e8f19e5be8586d545ad89e`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 11.9 KB (11900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26922604f711fbe11e4deec648f3e7a17a0ba6fb6f0214ff86e77ee65f107d`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:24c1acc54b417fb63a1d59b969f6218d5799a77cf20762a5b75670d5c1f6b6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:0d650b9aa64ccdccf2c0174fbbdaff6a190fa253cd43182abb9688b91ac2d8b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0f6839ea1166db97a20495fe610f28bab6623fa6b1555a98d30acfd7087a97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:32:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:32:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jan 2024 04:32:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:32:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:32:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:32:39 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:32:40 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:32:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:32:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:32:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ce22509b2a87df3de1734f9f1250513d18380876f4db91a30ac789a7781ad0`  
		Last Modified: Thu, 11 Jan 2024 04:33:50 GMT  
		Size: 5.2 MB (5228518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfba3eaa827dfd20bd3c8383e1be6d9e152f01c5d0265f8dc44ec4e2338e85e`  
		Last Modified: Thu, 11 Jan 2024 04:33:53 GMT  
		Size: 34.6 MB (34580777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e511276d45bc32b4775e49a3ba68e942d0548ed5e9c74cdbf4933504438f04d`  
		Last Modified: Thu, 11 Jan 2024 04:33:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f58b751b1682fab74c470d6e164666c1c1ce9e6ad8d952211287813f089219`  
		Last Modified: Thu, 11 Jan 2024 04:33:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0bd14f309fb859895bc116947add2ec5349a549c5bd67fb553cb286d314640`  
		Last Modified: Thu, 11 Jan 2024 04:33:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a592c6abb5b3e689f1fbbb4fc8ad0ee301f50f5141a8da86e794ebf4373098da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63849323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a963827a0df6ac65b61aaa7b0e83ae44b57a945ae7ed225491c1b53b76687cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:37:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:37:22 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jan 2024 03:37:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:37:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:37:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:37:34 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:37:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:37:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:37:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:37:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb335c60237940ef5e6da9b84af94c4a1ee1339486a685aa03f3ba6138c3db`  
		Last Modified: Thu, 11 Jan 2024 03:39:07 GMT  
		Size: 4.5 MB (4493773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c545284751211488b480657a766c15bc5be02742185d989a7b7f88b90ce60b4e`  
		Last Modified: Thu, 11 Jan 2024 03:39:12 GMT  
		Size: 32.8 MB (32752185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8674ff43974559bdbbe711bc58a663be3c045fcdbbac8059f1bb276d72d9dc8b`  
		Last Modified: Thu, 11 Jan 2024 03:39:06 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558afdb934e92800b7e15b6d92fb670f703632d5d43dc225039fb7c8a19727e`  
		Last Modified: Thu, 11 Jan 2024 03:39:06 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5902adecb7d68f2617a963525ddbfcdb35fbcd29d6df8f8c296ab9c240dd051e`  
		Last Modified: Thu, 11 Jan 2024 03:39:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:388e3dd9ef6bc237db8eab1be4e6233b5c4f0a24e4a8c36efea7d9d38e6c8ef2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67945348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf66dee867e2676924c07f4c3e38ba78e6e210151b958ed57dc92750070827d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:51:46 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 19 Dec 2023 06:51:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:51:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:51:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:51:52 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:51:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:51:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:51:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:51:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc66c48b7a65841496b979a76be7702db24db3c80de076ea9e60d682843b833`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 5.2 MB (5210839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405c1420195784b90952e5fc70b84b760f274a2123bfb71b22186ce7894a2831`  
		Last Modified: Tue, 19 Dec 2023 06:52:45 GMT  
		Size: 32.6 MB (32646053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67642cc71f0181eae5adad8a805ef277c77e656449325fcbdd3b2709124df2af`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c9b3552334ef4a184fd32a62063119a1f74a4a38bc6e566430fd9ee07c4cc`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77785dcdbc20de8fff3ade8a7824f47118ee666385c9a8134d00431b0be64171`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:dd594d6c3ce78de050cafbe947ae9160e219fac5f6c495170152e273bbb6539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d443ad920eb374ee66690c74c337d683f10acbf098652ccea13ff66e443859a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775cfdac12b0e12818f11a357b296bfda47308d5c4c59ed0c4da13a533c95ea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:35:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:35:58 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 01 Dec 2023 06:36:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:04 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:04 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:04 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b6362e68ff3f80ca0f4dfc4b18ec97abba97d0095553e5de9a503854d2629`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 284.9 KB (284927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c0da1c051ed2f9a5a22947f1d58543c32f2f57c14bc2f5e67613562ac2f80`  
		Last Modified: Fri, 01 Dec 2023 06:36:58 GMT  
		Size: 19.2 MB (19204187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62705dd567c9238c5ff5284062e0f188d2fd24e7fbd76c28b0c519c62a064982`  
		Last Modified: Fri, 01 Dec 2023 06:36:55 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f371150413256e224b5688283c65843b2112f42ba96afb2c8ac88427b71d8a`  
		Last Modified: Fri, 01 Dec 2023 06:36:55 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259ccd9cb6a3a0f14021a1a53e5639d87755306dd5d37a4775b7cb5a597b8ee9`  
		Last Modified: Fri, 01 Dec 2023 06:36:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:24c1acc54b417fb63a1d59b969f6218d5799a77cf20762a5b75670d5c1f6b6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:0d650b9aa64ccdccf2c0174fbbdaff6a190fa253cd43182abb9688b91ac2d8b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71251635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0f6839ea1166db97a20495fe610f28bab6623fa6b1555a98d30acfd7087a97`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:32:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:32:32 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jan 2024 04:32:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:32:39 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:32:39 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:32:39 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:32:40 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:32:40 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:32:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:32:40 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ce22509b2a87df3de1734f9f1250513d18380876f4db91a30ac789a7781ad0`  
		Last Modified: Thu, 11 Jan 2024 04:33:50 GMT  
		Size: 5.2 MB (5228518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccfba3eaa827dfd20bd3c8383e1be6d9e152f01c5d0265f8dc44ec4e2338e85e`  
		Last Modified: Thu, 11 Jan 2024 04:33:53 GMT  
		Size: 34.6 MB (34580777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e511276d45bc32b4775e49a3ba68e942d0548ed5e9c74cdbf4933504438f04d`  
		Last Modified: Thu, 11 Jan 2024 04:33:49 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f58b751b1682fab74c470d6e164666c1c1ce9e6ad8d952211287813f089219`  
		Last Modified: Thu, 11 Jan 2024 04:33:49 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e0bd14f309fb859895bc116947add2ec5349a549c5bd67fb553cb286d314640`  
		Last Modified: Thu, 11 Jan 2024 04:33:49 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:a592c6abb5b3e689f1fbbb4fc8ad0ee301f50f5141a8da86e794ebf4373098da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63849323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a963827a0df6ac65b61aaa7b0e83ae44b57a945ae7ed225491c1b53b76687cf`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:37:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:37:22 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 11 Jan 2024 03:37:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:37:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:37:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:37:34 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:37:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:37:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:37:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:37:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb335c60237940ef5e6da9b84af94c4a1ee1339486a685aa03f3ba6138c3db`  
		Last Modified: Thu, 11 Jan 2024 03:39:07 GMT  
		Size: 4.5 MB (4493773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c545284751211488b480657a766c15bc5be02742185d989a7b7f88b90ce60b4e`  
		Last Modified: Thu, 11 Jan 2024 03:39:12 GMT  
		Size: 32.8 MB (32752185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8674ff43974559bdbbe711bc58a663be3c045fcdbbac8059f1bb276d72d9dc8b`  
		Last Modified: Thu, 11 Jan 2024 03:39:06 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c558afdb934e92800b7e15b6d92fb670f703632d5d43dc225039fb7c8a19727e`  
		Last Modified: Thu, 11 Jan 2024 03:39:06 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5902adecb7d68f2617a963525ddbfcdb35fbcd29d6df8f8c296ab9c240dd051e`  
		Last Modified: Thu, 11 Jan 2024 03:39:06 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:388e3dd9ef6bc237db8eab1be4e6233b5c4f0a24e4a8c36efea7d9d38e6c8ef2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67945348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf66dee867e2676924c07f4c3e38ba78e6e210151b958ed57dc92750070827d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:51:46 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Tue, 19 Dec 2023 06:51:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:51:51 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:51:51 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:51:52 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:51:52 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:51:52 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:51:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:51:52 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc66c48b7a65841496b979a76be7702db24db3c80de076ea9e60d682843b833`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 5.2 MB (5210839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:405c1420195784b90952e5fc70b84b760f274a2123bfb71b22186ce7894a2831`  
		Last Modified: Tue, 19 Dec 2023 06:52:45 GMT  
		Size: 32.6 MB (32646053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67642cc71f0181eae5adad8a805ef277c77e656449325fcbdd3b2709124df2af`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c9b3552334ef4a184fd32a62063119a1f74a4a38bc6e566430fd9ee07c4cc`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77785dcdbc20de8fff3ade8a7824f47118ee666385c9a8134d00431b0be64171`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:dd594d6c3ce78de050cafbe947ae9160e219fac5f6c495170152e273bbb6539c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d443ad920eb374ee66690c74c337d683f10acbf098652ccea13ff66e443859a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22893117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775cfdac12b0e12818f11a357b296bfda47308d5c4c59ed0c4da13a533c95ea6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:35:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:35:58 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Fri, 01 Dec 2023 06:36:03 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:04 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:04 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:04 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:04 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:04 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b6362e68ff3f80ca0f4dfc4b18ec97abba97d0095553e5de9a503854d2629`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 284.9 KB (284927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764c0da1c051ed2f9a5a22947f1d58543c32f2f57c14bc2f5e67613562ac2f80`  
		Last Modified: Fri, 01 Dec 2023 06:36:58 GMT  
		Size: 19.2 MB (19204187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62705dd567c9238c5ff5284062e0f188d2fd24e7fbd76c28b0c519c62a064982`  
		Last Modified: Fri, 01 Dec 2023 06:36:55 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f371150413256e224b5688283c65843b2112f42ba96afb2c8ac88427b71d8a`  
		Last Modified: Fri, 01 Dec 2023 06:36:55 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259ccd9cb6a3a0f14021a1a53e5639d87755306dd5d37a4775b7cb5a597b8ee9`  
		Last Modified: Fri, 01 Dec 2023 06:36:55 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:cc52d5d53e61605ff0cbf2ebb18ad059b1f845700678ec1579a4507ff28cf6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:5d8906e1a4ae20c95a86f194f3265708f833ba28e6ca8483970e33876499511c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71899112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9494e4f0f181ce2c087fa86ec61edac2f7de99494e4899af67170c8a3882e02c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:32:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:32:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jan 2024 04:32:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:32:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:32:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:32:55 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:32:55 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:32:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:32:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:32:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ce22509b2a87df3de1734f9f1250513d18380876f4db91a30ac789a7781ad0`  
		Last Modified: Thu, 11 Jan 2024 04:33:50 GMT  
		Size: 5.2 MB (5228518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6872c1939a8ca1b69bd7a5e8cc7986c7b8dc848d08c1631e8d6f6af1c82febc0`  
		Last Modified: Thu, 11 Jan 2024 04:34:06 GMT  
		Size: 35.2 MB (35228254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c49985357f0fce2ba7ec9f505e7efe15538b0ba0b4dd34f4eba89bb2a62ab7`  
		Last Modified: Thu, 11 Jan 2024 04:34:02 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6769bb40b9c1c873574b36426fa9bf6e11d9e8de0995647e7050322f33e60b`  
		Last Modified: Thu, 11 Jan 2024 04:34:02 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffc7bc275e345a96492ab60f9e07e237686baa5057fca9ce1eae28ab580c36`  
		Last Modified: Thu, 11 Jan 2024 04:34:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0eb22b1727f58dcb0a1c908d31d2ed17d41825ca9d69a19df17213ba7a61f668
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64625447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad42f021fb214603535ecfa44847607f07798edfaec1761291d808e63fa0bc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:37:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:37:43 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jan 2024 03:37:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:37:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:37:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:37:56 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:37:56 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:37:56 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:37:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:37:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb335c60237940ef5e6da9b84af94c4a1ee1339486a685aa03f3ba6138c3db`  
		Last Modified: Thu, 11 Jan 2024 03:39:07 GMT  
		Size: 4.5 MB (4493773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef7724f986b0bfb3afa6acb6d756955b4dba81d00e257c2d65c210c6184400`  
		Last Modified: Thu, 11 Jan 2024 03:39:28 GMT  
		Size: 33.5 MB (33528313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdb30837f287600301bd1f8f165dbf08e731e566b9064996f98346d79e04de8`  
		Last Modified: Thu, 11 Jan 2024 03:39:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bcb3e394451edeca8ff80db98edc8708f13d24863e115e096a1a17fd9e5565`  
		Last Modified: Thu, 11 Jan 2024 03:39:21 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703121abd07ef3270cee13ef821e862dc702770bf0397ff15e96d1ebe1c41a8`  
		Last Modified: Thu, 11 Jan 2024 03:39:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fe2ddf610dbea48d463714296de718c414ef93373ebc3ec6f967c54b91b3908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68698065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856a5bdc65d8cf8e538cc77df8dd0c5cae4adeea157a9a00bb4f63dcaa7c354b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:51:56 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 19 Dec 2023 06:52:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:52:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:52:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:52:02 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:52:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:52:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:52:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc66c48b7a65841496b979a76be7702db24db3c80de076ea9e60d682843b833`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 5.2 MB (5210839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462720853cc19643db0b312120aaaf8a1515d2c553fc34b615db5800994aaa59`  
		Last Modified: Tue, 19 Dec 2023 06:52:56 GMT  
		Size: 33.4 MB (33398777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c22aa179e33717340b1e8775e7bdd47184a81c0a17b080711895583f9a8473c`  
		Last Modified: Tue, 19 Dec 2023 06:52:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abce1088f5808a314e180c782d96c84c8a0ab8c75e93b88a3e9b8eca00fda031`  
		Last Modified: Tue, 19 Dec 2023 06:52:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a1536f2670c4bc7f443d9f6d7cd4412430f2f976681323a5406cdb45d86fb`  
		Last Modified: Tue, 19 Dec 2023 06:52:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:5f02388edda6af9d9bb46b854713ec96f992d844534ceea4812d73c135e14b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:cc829c177999437ba22781298fba995694ac45f861d53297f52d5990204f1119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af67748adebd37700137ca0f84683caf8f79936677baa935f4e4517101c8a4e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:35:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:36:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 01 Dec 2023 06:36:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:15 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:15 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b6362e68ff3f80ca0f4dfc4b18ec97abba97d0095553e5de9a503854d2629`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 284.9 KB (284927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc488697b801418eec841f12ba3d89bf046fe5a8871026627df8c7b18bbf3c2`  
		Last Modified: Fri, 01 Dec 2023 06:37:10 GMT  
		Size: 19.7 MB (19672196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0059199d07297cece7ba047ec7597c67265fa549c0dc97ea36b37ca5d8d8b7`  
		Last Modified: Fri, 01 Dec 2023 06:37:07 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cce2668ed03521702eeee993943b00ac1b0afe7a8552913b63730db476f3aa6`  
		Last Modified: Fri, 01 Dec 2023 06:37:07 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce797caba36698bbbe4778fc612b467a093edd2efae91afac36fe9ad0f1cd29`  
		Last Modified: Fri, 01 Dec 2023 06:37:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:cc52d5d53e61605ff0cbf2ebb18ad059b1f845700678ec1579a4507ff28cf6c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:5d8906e1a4ae20c95a86f194f3265708f833ba28e6ca8483970e33876499511c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71899112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9494e4f0f181ce2c087fa86ec61edac2f7de99494e4899af67170c8a3882e02c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:38:16 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Thu, 11 Jan 2024 02:38:17 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:32:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:32:47 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jan 2024 04:32:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:32:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:32:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:32:55 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:32:55 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:32:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:32:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:32:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ce22509b2a87df3de1734f9f1250513d18380876f4db91a30ac789a7781ad0`  
		Last Modified: Thu, 11 Jan 2024 04:33:50 GMT  
		Size: 5.2 MB (5228518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6872c1939a8ca1b69bd7a5e8cc7986c7b8dc848d08c1631e8d6f6af1c82febc0`  
		Last Modified: Thu, 11 Jan 2024 04:34:06 GMT  
		Size: 35.2 MB (35228254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08c49985357f0fce2ba7ec9f505e7efe15538b0ba0b4dd34f4eba89bb2a62ab7`  
		Last Modified: Thu, 11 Jan 2024 04:34:02 GMT  
		Size: 12.2 KB (12243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef6769bb40b9c1c873574b36426fa9bf6e11d9e8de0995647e7050322f33e60b`  
		Last Modified: Thu, 11 Jan 2024 04:34:02 GMT  
		Size: 11.9 KB (11902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffc7bc275e345a96492ab60f9e07e237686baa5057fca9ce1eae28ab580c36`  
		Last Modified: Thu, 11 Jan 2024 04:34:02 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:0eb22b1727f58dcb0a1c908d31d2ed17d41825ca9d69a19df17213ba7a61f668
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64625447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad42f021fb214603535ecfa44847607f07798edfaec1761291d808e63fa0bc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:37 GMT
ADD file:1a36d919bfcbaa6b981b71ce99d777d303e69c2d6cb1924992e5a9cd811c11c5 in / 
# Thu, 11 Jan 2024 02:42:38 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:37:22 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:37:43 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 11 Jan 2024 03:37:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:37:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:37:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:37:56 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:37:56 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:37:56 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:37:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:37:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:d976170654fe1bc717306b8bf14dc57d20e331b13e4797bc137e6911aa745a8a`  
		Last Modified: Thu, 11 Jan 2024 02:49:26 GMT  
		Size: 26.6 MB (26578974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8eb335c60237940ef5e6da9b84af94c4a1ee1339486a685aa03f3ba6138c3db`  
		Last Modified: Thu, 11 Jan 2024 03:39:07 GMT  
		Size: 4.5 MB (4493773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ef7724f986b0bfb3afa6acb6d756955b4dba81d00e257c2d65c210c6184400`  
		Last Modified: Thu, 11 Jan 2024 03:39:28 GMT  
		Size: 33.5 MB (33528313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cdb30837f287600301bd1f8f165dbf08e731e566b9064996f98346d79e04de8`  
		Last Modified: Thu, 11 Jan 2024 03:39:21 GMT  
		Size: 12.2 KB (12244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18bcb3e394451edeca8ff80db98edc8708f13d24863e115e096a1a17fd9e5565`  
		Last Modified: Thu, 11 Jan 2024 03:39:21 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7703121abd07ef3270cee13ef821e862dc702770bf0397ff15e96d1ebe1c41a8`  
		Last Modified: Thu, 11 Jan 2024 03:39:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:8fe2ddf610dbea48d463714296de718c414ef93373ebc3ec6f967c54b91b3908
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68698065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856a5bdc65d8cf8e538cc77df8dd0c5cae4adeea157a9a00bb4f63dcaa7c354b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:51:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:51:56 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Tue, 19 Dec 2023 06:52:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:52:01 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:52:01 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:52:02 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:52:02 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:52:02 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:52:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:52:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc66c48b7a65841496b979a76be7702db24db3c80de076ea9e60d682843b833`  
		Last Modified: Tue, 19 Dec 2023 06:52:42 GMT  
		Size: 5.2 MB (5210839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462720853cc19643db0b312120aaaf8a1515d2c553fc34b615db5800994aaa59`  
		Last Modified: Tue, 19 Dec 2023 06:52:56 GMT  
		Size: 33.4 MB (33398777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c22aa179e33717340b1e8775e7bdd47184a81c0a17b080711895583f9a8473c`  
		Last Modified: Tue, 19 Dec 2023 06:52:53 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abce1088f5808a314e180c782d96c84c8a0ab8c75e93b88a3e9b8eca00fda031`  
		Last Modified: Tue, 19 Dec 2023 06:52:53 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798a1536f2670c4bc7f443d9f6d7cd4412430f2f976681323a5406cdb45d86fb`  
		Last Modified: Tue, 19 Dec 2023 06:52:53 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:5f02388edda6af9d9bb46b854713ec96f992d844534ceea4812d73c135e14b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:cc829c177999437ba22781298fba995694ac45f861d53297f52d5990204f1119
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23361124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af67748adebd37700137ca0f84683caf8f79936677baa935f4e4517101c8a4e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:58 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Thu, 30 Nov 2023 23:22:59 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:22:09 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:35:47 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:36:09 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Fri, 01 Dec 2023 06:36:14 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:15 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:15 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:15 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:15 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:15 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:15 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:15 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae43a7dfb488bfdf09941272691a16afeb9a0ec5f2aeb3afb906b9e61d0eea0`  
		Last Modified: Fri, 01 Dec 2023 05:24:18 GMT  
		Size: 276.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916b6362e68ff3f80ca0f4dfc4b18ec97abba97d0095553e5de9a503854d2629`  
		Last Modified: Fri, 01 Dec 2023 06:36:42 GMT  
		Size: 284.9 KB (284927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcc488697b801418eec841f12ba3d89bf046fe5a8871026627df8c7b18bbf3c2`  
		Last Modified: Fri, 01 Dec 2023 06:37:10 GMT  
		Size: 19.7 MB (19672196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0059199d07297cece7ba047ec7597c67265fa549c0dc97ea36b37ca5d8d8b7`  
		Last Modified: Fri, 01 Dec 2023 06:37:07 GMT  
		Size: 12.3 KB (12265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cce2668ed03521702eeee993943b00ac1b0afe7a8552913b63730db476f3aa6`  
		Last Modified: Fri, 01 Dec 2023 06:37:07 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce797caba36698bbbe4778fc612b467a093edd2efae91afac36fe9ad0f1cd29`  
		Last Modified: Fri, 01 Dec 2023 06:37:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:88a8f3c11c35918ccc4a79107520e7f94b36f71b4272af23f0e2bac83946079b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d6106695cafa72d587ab758ad5ea255d1a107f703cdebb5716e25070668b6cbb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 MB (31559386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9f8d7783b4d1c122bc59b5d25e257c5c705b48e80425b1ca30c9b862f62e66`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 05:23:13 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:36:21 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Fri, 01 Dec 2023 06:36:21 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Fri, 01 Dec 2023 06:36:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Fri, 01 Dec 2023 06:36:27 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Fri, 01 Dec 2023 06:36:27 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Fri, 01 Dec 2023 06:36:27 GMT
EXPOSE 8888
# Fri, 01 Dec 2023 06:36:28 GMT
VOLUME [/var/lib/chronograf]
# Fri, 01 Dec 2023 06:36:28 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Fri, 01 Dec 2023 06:36:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 01 Dec 2023 06:36:28 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703e958f39c4082f015dd7de32b1c116ef56e1e54010a31e991ec0c10e7feecc`  
		Last Modified: Fri, 01 Dec 2023 05:25:29 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:822880f5cd7c4ada55339070e05a9bbdebfa8ffe320d8e04ef9484a76cce73b1`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 284.7 KB (284691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3f1f8f312b84a559d6c230bd8b16e0bc3c2fa9b0d8b5f82500f63f436f293e`  
		Last Modified: Fri, 01 Dec 2023 06:37:24 GMT  
		Size: 27.8 MB (27847590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d9203360be51e26b6712f778d3e1d01a81b99f995a63bb39ac3fcfaee792a4d`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 12.3 KB (12268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befa6d5fb571ce4e663b4dcb70d144cd0146fa42d8f0b9eb984e9351607ff065`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 11.9 KB (11899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4266056d57960899ab7424d6866e7b2ba4e13e493e9f7beb955eebcbac4d907`  
		Last Modified: Fri, 01 Dec 2023 06:37:19 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:1564fb1891f23f9d03a7e24adbc1cf788295c855cf3a0dbf65ac5e8a484bcec3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:8a36118ae02c06a5523732169ff5a97976c5abde96792f9e2cc8f1ffacce0b46
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84073337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d0df62239302e1f6ecb647e8fbb91eda4cc29c02c59ba0006ebcb558742769d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:37:54 GMT
ADD file:9deb26e1dbc258df47629e6f8fbcea4e4b54e7673537cc925db16af858d9cc8d in / 
# Thu, 11 Jan 2024 02:37:54 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 04:33:10 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 04:33:10 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Thu, 11 Jan 2024 04:33:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 04:33:18 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 04:33:18 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 04:33:18 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 04:33:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 04:33:18 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:2f44b7a888fa005d07c031d3cfad2a1c0344207def2ab9dbb97712425ff812c1`  
		Last Modified: Thu, 11 Jan 2024 02:42:28 GMT  
		Size: 29.1 MB (29125921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46513bb8447bc150084803d26f4c182db6258f58f1b1d4a5119879af7f055b54`  
		Last Modified: Thu, 11 Jan 2024 04:34:17 GMT  
		Size: 7.9 MB (7870172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de2094287552144254685d6024bfab813dbf44032b509244630b93a75be4645`  
		Last Modified: Thu, 11 Jan 2024 04:34:21 GMT  
		Size: 47.1 MB (47052856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0381ea74b82acae59b5c3208bbc176f7ba607263be258559c93d973cebac476b`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b80052a70e74ab35a78203e3c82aef19cde6e5f546af67b9a97d3db5532849`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91091f4813580d8b81a77240fcd055cef92638d713a87feda438abd423ef2039`  
		Last Modified: Thu, 11 Jan 2024 04:34:15 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:d003628994751531936cf990737f67d86023ce8dcb419fc6658aec7d2081c3e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75886321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3179d715357eba52a0692348fc22ddf7983cb0de165fa731480ecbe037184533`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 11 Jan 2024 02:42:07 GMT
ADD file:d365646158a0cbd9fd6557fb285ff54033d19efa44c8f46080998e8a603120a0 in / 
# Thu, 11 Jan 2024 02:42:07 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 03:38:20 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 11 Jan 2024 03:38:20 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Thu, 11 Jan 2024 03:38:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 11 Jan 2024 03:38:35 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 11 Jan 2024 03:38:36 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 11 Jan 2024 03:38:36 GMT
EXPOSE 8888
# Thu, 11 Jan 2024 03:38:36 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jan 2024 03:38:36 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 11 Jan 2024 03:38:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jan 2024 03:38:37 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:6e6fe5c6e33442e884612254cc97763ab9fa910c47faa20175f9edcaefda7316`  
		Last Modified: Thu, 11 Jan 2024 02:48:37 GMT  
		Size: 24.7 MB (24718126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01f7b9ecca0085cc54af13c89b81377d3f0b360a495fbf4d1aeaa85076c65f6`  
		Last Modified: Thu, 11 Jan 2024 03:39:38 GMT  
		Size: 6.5 MB (6494872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b1a6b2eaabab5ddb9bfb8f5f5a1c9bed36593aaa8561f40af782a013e350ce`  
		Last Modified: Thu, 11 Jan 2024 03:39:46 GMT  
		Size: 44.6 MB (44648935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19204c8b94fc7b4f9bc463de009cef206f893950e6608d636aa2b7b4ef8ab4`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 12.2 KB (12245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656346136ac769804ddc702b5a0cd72eb1d229031c58751d1ddca083917653a5`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 11.9 KB (11903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eadb16209259b77314b7dffab85374c70bd5cc8a6ff9b73c2d8b9e989f1b42`  
		Last Modified: Thu, 11 Jan 2024 03:39:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:5bd8a314f132697c0738b1448068b4e5ef4b90ec4526dc4250ad1cf1bf40d8ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.6 MB (81601551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2029fcba43958022c38bd47cf756be831228b0de5808b033f6352a846f37882`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:11 GMT
ADD file:262fd7bf0bc26e5d2a229fba52626e22b8a93beac29733acfc60e716c26e689d in / 
# Tue, 19 Dec 2023 01:41:11 GMT
CMD ["bash"]
# Tue, 19 Dec 2023 06:52:12 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Tue, 19 Dec 2023 06:52:12 GMT
ENV CHRONOGRAF_VERSION=1.10.2
# Tue, 19 Dec 2023 06:52:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Tue, 19 Dec 2023 06:52:19 GMT
EXPOSE 8888
# Tue, 19 Dec 2023 06:52:19 GMT
VOLUME [/var/lib/chronograf]
# Tue, 19 Dec 2023 06:52:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Tue, 19 Dec 2023 06:52:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 19 Dec 2023 06:52:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:24e221e92a36ab5b0075dd156b4f2ff095532a9b0927946cf6070bb1bea208b8`  
		Last Modified: Tue, 19 Dec 2023 01:44:38 GMT  
		Size: 29.2 MB (29157269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25528e50586e703a8d0b96794925dffd49a3c11ed5b28c7900efd2da177a3974`  
		Last Modified: Tue, 19 Dec 2023 06:53:06 GMT  
		Size: 7.6 MB (7646993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a25f7fddb0c4726b93b4c41f070fa5e979b9c974025e21868cdfbafb8f3ea7`  
		Last Modified: Tue, 19 Dec 2023 06:53:09 GMT  
		Size: 44.8 MB (44772890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44b645f60a59e0181445966b8f3291ed3823c834e51bdfc1c7ed5e5d9a587272`  
		Last Modified: Tue, 19 Dec 2023 06:53:05 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4746b4753b6df55eaf2ee32ac0882d4766ac6baa3259568c72ff5566a942a6`  
		Last Modified: Tue, 19 Dec 2023 06:53:05 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cab7e4479d3d188fc282ce7a406d2e216f222fe1f17ea23c496cbe6730249f78`  
		Last Modified: Tue, 19 Dec 2023 06:53:04 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
