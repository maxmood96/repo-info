## `clojure:temurin-24-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:9e267a242a7eb2d7d7f208779beff7d061f4a1cb7a3f131be2164eebdaa9186a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:891de911daced399591f0bda2f4cb781545530676cfbeb4d14381e23a69d7f6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187708840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62328e2706ce2e14aef1d0be0a1dec853dce403480277448c03102fe8be12d09`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f932987f6cec527ec8e6b988088e2374908a3a39de98196413ac9a6015caca`  
		Last Modified: Tue, 03 Jun 2025 05:14:19 GMT  
		Size: 90.0 MB (89952002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf28e21f65a337ffa25d61d57cb68b48d3b06f14ef52b3020e1f68abf9e4063b`  
		Last Modified: Tue, 03 Jun 2025 05:14:19 GMT  
		Size: 69.5 MB (69530471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54fee57e8033ec44170ee3bbfbebf6a784c44126f5cec3391cb0bd714e04444`  
		Last Modified: Tue, 03 Jun 2025 05:14:18 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:856fd792d528a619c2eee652dad181f527487d55f02a32ef4f9d60606bafa44f`  
		Last Modified: Tue, 03 Jun 2025 05:14:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2187836a7b8130d700756cfee06343d0755a599814d15570dcb09d2ce13f6087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16b0f0771915abdc74ae505eece408550832520c36dcc21ce6c4400177bc2951`

```dockerfile
```

-	Layers:
	-	`sha256:394f2de662d74c69b3f2ccbb47e28c976232260bb458ff0149007b2009d1e51c`  
		Last Modified: Tue, 03 Jun 2025 05:14:18 GMT  
		Size: 4.9 MB (4912144 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37cdfd117e20ee32500dda254dd6e908db8363b3715d022a4feb995702a757b4`  
		Last Modified: Tue, 03 Jun 2025 05:14:18 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e51ed09b2fb1bc0e72f8608249fba0ce297d06c5222d4fe7e5d13024f3050cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186543783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:978bc30766fc8bf140d8fec0bfc3e28c44167a3ddb34458bce57b57b7a0bb6df`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6817c00a35ed33ec5d0a26775ce61734765ce7050a5b559cfe2d379bcea015a1`  
		Last Modified: Thu, 22 May 2025 08:39:33 GMT  
		Size: 89.1 MB (89091257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265d1137a545bc4f1008b7e789d9d44023c6b77fa83b38c5d7fb34a79dafd215`  
		Last Modified: Thu, 22 May 2025 08:44:41 GMT  
		Size: 69.4 MB (69386205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696317182a64cbfd24b382a932050869b7aaea8503b7d296f87ca3dc2603bf87`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:539d49140e3a5f2282dfe3f6d265b8028a5cecf9f802db32206ff78eb88b32f6`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8ce06eb3a2051db236d5851c58dee97f450949cf263de88d0f0767c4bcf9da92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4933891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f915d96687c437e53473d3829cedd447fd8a89cffd10fc98d0d0d55a1781cb32`

```dockerfile
```

-	Layers:
	-	`sha256:cd9fd63028b6b1362138c2476fdb45cf06b284c2bdb055f3e18cf1bad02d2e49`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 4.9 MB (4917902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db4fc69174822246d9354792aa30eb6583b83b22ae2eb5734136ba5f7b6a9fb`  
		Last Modified: Thu, 22 May 2025 08:44:39 GMT  
		Size: 16.0 KB (15989 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:148f6ad14d3cc5a7777f198952a5611eeb7b1eacf14a879ca47af1463f32d43f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197335735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94180aa98c3517a03c04dcca2ba8afc12a3629da4067375aa644198042771ca7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Wed, 21 May 2025 22:28:16 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c800abde4be3e9e8b52b7f2cca28f339939a1b96650a19d358b45e7335484611`  
		Last Modified: Thu, 22 May 2025 11:43:28 GMT  
		Size: 89.9 MB (89920275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cbfb9849da87bedc4d2259ed525b380a84702d7e4d91d1a81d030130ebe2d2`  
		Last Modified: Thu, 22 May 2025 11:50:21 GMT  
		Size: 75.3 MB (75347507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224b11b5f1aa67f523d77663b114618dc691ff6df96c29af0d6a68be035275fe`  
		Last Modified: Thu, 22 May 2025 11:50:18 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29a714f9a98c7a9c680052a8a75a540259c98bd335f9606a91d1ce2ec73be1c3`  
		Last Modified: Thu, 22 May 2025 11:50:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2e506a276bbdb63311862745d464513035a933c77aaf090fa4d26a581bb289f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231e9b11aa3fe4e846f51f04a948cf6b1fd8e08eb4d84bf6715994fd8b7dc5ed`

```dockerfile
```

-	Layers:
	-	`sha256:d304143919c57ff3acd6df9fa1abfabb1d194ac5f1ac4c1a0447f5bd0fbd02a6`  
		Last Modified: Thu, 22 May 2025 11:50:19 GMT  
		Size: 4.9 MB (4918600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec1e73c7f4da460e911da2e0784715ed99d52ba74d65abd6a91677b415ab3ab8`  
		Last Modified: Thu, 22 May 2025 11:50:18 GMT  
		Size: 15.9 KB (15920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bookworm-slim` - linux; s390x

```console
$ docker pull clojure@sha256:f1c693c19373d0ca8060a2b4bf6db13587f5b01e958f7b20512908ab9aff63ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180427832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331304cbe6708f4881c4f952063368ea3d553754ceb1d13dd332a05de3eb2cdd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 13 May 2025 03:53:36 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Tue, 13 May 2025 03:53:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 13 May 2025 03:53:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 May 2025 03:53:36 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Tue, 13 May 2025 03:53:36 GMT
WORKDIR /tmp
# Tue, 13 May 2025 03:53:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 13 May 2025 03:53:36 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 13 May 2025 03:53:36 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 13 May 2025 03:53:36 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Wed, 21 May 2025 22:28:38 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b984f64a36288041a3c614f4a78a8680d1a70349b080261f6d6bd8de5660a8`  
		Last Modified: Tue, 03 Jun 2025 06:36:43 GMT  
		Size: 85.2 MB (85216876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649a5a7cd274dd8875f179ddbb2bca2b38108b730b8b95c3499e4d428890660e`  
		Last Modified: Tue, 03 Jun 2025 06:41:38 GMT  
		Size: 68.3 MB (68327108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dec3722bc2e46f738e0e869ceb21387b9660e97e2e261cecbce11e42b8fd71`  
		Last Modified: Tue, 03 Jun 2025 06:41:37 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad996deb94bd459e392150323a6b4e4eed5f2d32f58ab396f9b860ed22163423`  
		Last Modified: Tue, 03 Jun 2025 06:41:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b1ce887b18475872109ab58df152d6ab2df3b16c710fc8bcc27f3e8a0c805b73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4924777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5f31df8a1ec5c8f2429c6c6ec8e7bf975cb8566a1e11b5d4a73302857d9bc0`

```dockerfile
```

-	Layers:
	-	`sha256:31c2e4b8720ae34b4b758aaca7fef462503ce7b84bd20ad7a3b1d8ab119dc84f`  
		Last Modified: Tue, 03 Jun 2025 06:41:37 GMT  
		Size: 4.9 MB (4908905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05975a227ea884301c1f9d5daa44a0e5a5139252e892e28d7c39a95ac5dd6506`  
		Last Modified: Tue, 03 Jun 2025 06:41:37 GMT  
		Size: 15.9 KB (15872 bytes)  
		MIME: application/vnd.in-toto+json
