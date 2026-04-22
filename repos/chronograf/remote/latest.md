## `chronograf:latest`

```console
$ docker pull chronograf@sha256:0f07a3a3ef4e82deb075683f72a89d194d780f1805d5232622f5619854a12da9
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
$ docker pull chronograf@sha256:b789cc3f234aca70cbe48a1b756ccdae8e27e5249b4254d0b40768d5fb554504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98523348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76ace0fc98017a90832ebf70bbdb13b0b5b83fb6ccf5fc8558b4dab85b58ab5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:39:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Wed, 22 Apr 2026 01:40:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:40:03 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:40:03 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:ff86ea2e5edce334d19a34fbc65d1a511aa1fc823dba1110422f991aa56b44d4`  
		Last Modified: Wed, 22 Apr 2026 00:16:25 GMT  
		Size: 28.2 MB (28236252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890bcea591fcf347b2fbf1d61b2a6b1983750cd5d9049eeda31e36c124f50e82`  
		Last Modified: Wed, 22 Apr 2026 01:40:20 GMT  
		Size: 7.9 MB (7880761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e9a112a46a66d65e1f9fd68ce3b3bb69113b37aa907bb408f12f0fdd304ee8`  
		Last Modified: Wed, 22 Apr 2026 01:40:21 GMT  
		Size: 62.4 MB (62381869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba8a71fdbf6fb57d2ef3a4ee7881fa229d32585df420363632d945c6360bbaa`  
		Last Modified: Wed, 22 Apr 2026 01:40:20 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d9a90b228f0f58f48584d9b66a142f7f4511640878b26c8cf83e1a8cfddeba`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 11.9 KB (11906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d54185746004b87475a722a316bd05ef4ef68c46df2d550d1fa851031c7b511`  
		Last Modified: Wed, 22 Apr 2026 01:40:21 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:b6de94af8207cd47c082d6404c39429ed5d2c1fd8dd8c89f1f8ce7181c3bf707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7411f7288317e0e8573591b761771a9f6586041704aca4e3a8cb098c4717b7`

```dockerfile
```

-	Layers:
	-	`sha256:aa00abfb671c2cd3e6adb2c094a43dea281dd9b55f0c7434ac77dd8fe565fa5a`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 2.9 MB (2873700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:852da94dc4b795b75cd9dd711b2e24141e43edbb44df342a56361a3f11e96403`  
		Last Modified: Wed, 22 Apr 2026 01:40:19 GMT  
		Size: 16.1 KB (16085 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:7f6ba8a05e8752787341b7fe2a6a74810b06aa9fa70a1a0228f775cc695b037a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.8 MB (76798073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:930d1c377ac04e3da986523b9e03970d9aff20f8036670f211d374ae5e6e562c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 02:04:31 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENV CHRONOGRAF_VERSION=1.10.9
# Tue, 07 Apr 2026 02:04:39 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
EXPOSE map[8888/tcp:{}]
# Tue, 07 Apr 2026 02:04:39 GMT
VOLUME [/var/lib/chronograf]
# Tue, 07 Apr 2026 02:04:39 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 07 Apr 2026 02:04:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 07 Apr 2026 02:04:39 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:dabf2c04988ff47a9777c2e6aee85c1e347525704928c5c1a366fae1fb63fea2`  
		Last Modified: Tue, 07 Apr 2026 00:58:55 GMT  
		Size: 23.9 MB (23941461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde4224141eb326416434e57e6985960fa0299c171636ec51c978d7483ded221`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 6.5 MB (6512130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39644797429280d1790a41b83be262964fe685b66a13098f85a2830ef136af23`  
		Last Modified: Tue, 07 Apr 2026 02:04:51 GMT  
		Size: 46.3 MB (46320009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038716dc519bd0d53565ee9d170bb27389cee982f799ed02c5b30bb400da63b`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2857e0024941e8431e0d2e7288ff873bb60af2b99250a6c109fb700e616232c`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac7ccabd4f0e669d232e23f27536a4797faec571f1d5b385e8d37e9543ad1d4`  
		Last Modified: Tue, 07 Apr 2026 02:04:50 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:d033ac4c98bc3deb3c46315bff42913e431c32321890ec7914cd6b43bf0a4454
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a769173f691e7dbe1bbac685b1b6d2cf8af5e40c11a7536386e603ca5e558e45`

```dockerfile
```

-	Layers:
	-	`sha256:dff92a3ce28b58e918bb8a1b393141f0d15f0a7436d538d1b53bafdf3cd2f3f0`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 2.9 MB (2858027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29723eb32c4a4046b83b01b8e97bd5b93cfc334f24c3dcc9145d178038a36230`  
		Last Modified: Tue, 07 Apr 2026 02:04:49 GMT  
		Size: 16.2 KB (16170 bytes)  
		MIME: application/vnd.in-toto+json

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:68bafb55be081cc169b6026b419c1b5099ae8ef2e77f47aa67e3c7ff58147294
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95219034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4803eb94c2953dcc9b712710b6fea86b3bd3a5e49fbde785e8382ddfa648d9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:43:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENV CHRONOGRAF_VERSION=1.11.1
# Wed, 22 Apr 2026 01:43:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
EXPOSE map[8888/tcp:{}]
# Wed, 22 Apr 2026 01:43:35 GMT
VOLUME [/var/lib/chronograf]
# Wed, 22 Apr 2026 01:43:35 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Wed, 22 Apr 2026 01:43:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 22 Apr 2026 01:43:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:46ac7a0b9811e518f6b5a0d52940c913a1a560a8f78b82267804914e50244d2d`  
		Last Modified: Wed, 22 Apr 2026 00:16:03 GMT  
		Size: 28.1 MB (28116114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3890b2677d0421ab5024893da8a9b87e11e51d5f038697a769872acc46f8eb7e`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 7.7 MB (7698505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7f6bc004ebdfde070c98dd879bd60eb2e8b2fbbf8654cc3744687bb91b130e`  
		Last Modified: Wed, 22 Apr 2026 01:43:52 GMT  
		Size: 59.4 MB (59379943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:845367a4d5112966d659b3a767e8faeacdf77ea0d336f1ce3fe6f93b073136ee`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de84aba6d85fdb6b285d5b67445704e4f6badf59ba839f689b26293863eb6114`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba017d4f8fdb0864069f3dec705f13b4f4dc337b21b5fbb084810cebebd8e167`  
		Last Modified: Wed, 22 Apr 2026 01:43:51 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:c1d1173625df32d5f717779696e450af1183fae65fec15885bbbf79afd74ca5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d5cf482b920081a833f634b3740f5afacd4742f2fe22e955ad0d01826ef97d2`

```dockerfile
```

-	Layers:
	-	`sha256:f5caf2dd8813129b9c4c95cdbf9475460c6671d9b69076c9e01ff6fb31a12d18`  
		Last Modified: Wed, 22 Apr 2026 01:43:50 GMT  
		Size: 2.9 MB (2872914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2522c54541b05c9d9fe6b86bcfddd0e313001f46fd9647c6b93e4f5b2a456e`  
		Last Modified: Wed, 22 Apr 2026 01:43:49 GMT  
		Size: 16.2 KB (16191 bytes)  
		MIME: application/vnd.in-toto+json
