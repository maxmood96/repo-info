## `chronograf:latest`

```console
$ docker pull chronograf@sha256:2aa9fb24f733b4d04e164d25f5ef96980c3b581ddab5c50857d1fdb42d222089
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
$ docker pull chronograf@sha256:73202e652dda47453c6e05e29ca9be91761dcc92f64682de2e149a3d0a622a36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96342670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27932b95b4e46a21c3c4b00e9535bbe9d7155a6a5128abdac0e17faac5c5c816`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:42:55 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:43:02 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:43:02 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:43:02 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:43:02 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:43:02 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b9136609bef0128191aa157637b98dd7b98e52154ca60c18258d65957a01c6d0`  
		Last Modified: Wed, 10 Jun 2026 23:39:54 GMT  
		Size: 28.2 MB (28237624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556c9fe7644e1166887620855e94c2fba32d97d5e3ed4df537f06c1884a7f0ae`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 7.9 MB (7883267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55cf3f7752999b38e3d9223912ce753e63b747ba0ca49f8df5e319c088063e9`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 60.2 MB (60197307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5769e0d1dcfbaa03829bf62a9018e38189487c8fe5cde7c33ecf939c2b143f7e`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e438f602a3cd637900418a3cae8b6eb964b101379fb8aa88f21114895f23481`  
		Last Modified: Thu, 11 Jun 2026 00:43:14 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b16275212f52100b6eafaf66aa0d7343a79c7ce9ce1ca94ef1ea4dd3aba17d`  
		Last Modified: Thu, 11 Jun 2026 00:43:16 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:2c377acca3100b8eded8237f5294e94e498c9d60115575d43098702c544aab82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07de8db60e77546e14d4ee2975da7c7da016d1f475ba6cdc862591a303a9a83e`

```dockerfile
```

-	Layers:
	-	`sha256:2625568072a9dd1c4abcd0c7a987dab62a3e6c1f9f0afcb55d1ca787025eada8`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
		Size: 2.9 MB (2873738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e92aee71ca4c730a54e0d2b4d449e648529f3c9cf1d08c370c6c63ffc0cf073`  
		Last Modified: Thu, 11 Jun 2026 00:43:15 GMT  
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
$ docker pull chronograf@sha256:366675e696db69e613db19076980c8908e9b58729a1847e6749ffe90c20dab8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93055462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459b3796796fdfea3d602ce56fab1cc2c29954072f40d70adc290142e4fb3f8a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 00:44:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         24C975CBA61A024EE1B631787C3D57159FC2F927 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENV CHRONOGRAF_VERSION=1.11.3
# Thu, 11 Jun 2026 00:44:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY LICENSE /usr/share/chronograf/LICENSE # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
COPY agpl-3.0.md /usr/share/chronograf/agpl-3.0.md # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
EXPOSE map[8888/tcp:{}]
# Thu, 11 Jun 2026 00:44:47 GMT
VOLUME [/var/lib/chronograf]
# Thu, 11 Jun 2026 00:44:47 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Thu, 11 Jun 2026 00:44:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 11 Jun 2026 00:44:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:402614bd39aaec1e4bdcf25aa67f88588fc8d93997a2551c4e130e6ed2b06c7a`  
		Last Modified: Wed, 10 Jun 2026 23:39:57 GMT  
		Size: 28.1 MB (28122307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cbdd8fdc217506b94f451fe694a7434259077980dbfce32d678a110b1d5a084`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 7.7 MB (7699815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d99986976f45e221d9b9536bb7d61740629e2e34f15c8c96d9f4b700bff729`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 57.2 MB (57208871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694ce58a5f420870f543a6533816a87c9081c6d337adb50dc9b0fe82bec5ec9d`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 12.2 KB (12247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a236533c741fb74910832ada4193e1b28ee7b4538e09f17c736fc033514e8c51`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08405dd5bfe3886ba00084d0d4013c2b5840b2fea056cdcea79f498c5bcd2084`  
		Last Modified: Thu, 11 Jun 2026 00:45:02 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `chronograf:latest` - unknown; unknown

```console
$ docker pull chronograf@sha256:070e47966d05c2d6ad9490421a9ea383cd4c75362b29b8a8a4dc8548fd72f921
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2889144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40398e85b3e847b5bc169b9a9120493fbe744a1c8ec58c0b8bc92cc77725a6bf`

```dockerfile
```

-	Layers:
	-	`sha256:4cc86ee46eff59029c08f7a731845be8bf30156058866c32b2ae52c16c96560b`  
		Last Modified: Thu, 11 Jun 2026 00:45:01 GMT  
		Size: 2.9 MB (2872952 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c6deb7e17d185253c508ce914f5f9b2c1c20fb44f7b9fa7fbb5528837f1745`  
		Last Modified: Thu, 11 Jun 2026 00:45:00 GMT  
		Size: 16.2 KB (16192 bytes)  
		MIME: application/vnd.in-toto+json
