## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:c69cd4da26cd3a3ea3ec8eee29856c1c0f5d2dc483b0ddfc33925645c29e7b6b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:d03d6633ae49390f1a6a45a0d0a533e4fdc45249996e139f84d92a1b85638bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226532913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee6cedde7fee0c236b313a8916f9ff29536fbdd5368bf1961a81fcf070385a1`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb0ae134c5dc9c70f1521baa286f1a87030b23015ae910130b144316bd57a8ad`  
		Last Modified: Tue, 24 Dec 2024 22:37:17 GMT  
		Size: 103.6 MB (103633936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121d5aa64a742b63e1859775bb29f5c5f5184e41edd2bbe594c5ea25aebb5bf0`  
		Last Modified: Tue, 24 Dec 2024 22:37:21 GMT  
		Size: 69.2 MB (69159376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0d1ca7fdc2bbaa88742d84d2ba0efaf2ddba882433969d5dd0b31d4be69320`  
		Last Modified: Tue, 24 Dec 2024 22:37:14 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:9fbf03b51425b7d523f25bcab10b5d015fadd764c35a0d135599d613d2dad3b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7340954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cee9c7615edb3b1e857c9f2068e4ddeba543b20abe294cf7a625056eff80edf`

```dockerfile
```

-	Layers:
	-	`sha256:8db69a90eb5225044aad53b78662baa8ded7b74319236713fccd80e8528978b4`  
		Last Modified: Tue, 24 Dec 2024 22:37:15 GMT  
		Size: 7.3 MB (7326713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd60991c614df4e4d41de76f4397795745282c9c54723a7dcafa26ba63fb913`  
		Last Modified: Tue, 24 Dec 2024 22:37:14 GMT  
		Size: 14.2 KB (14241 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aae5459001181a77473e40650cf90309c6bd27f5ffa7e185e9100eeddb5d44ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224280352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9034230f18dd3d503a0280f1ff6a84c225942a5e1e96dc15363711d9e2e9a9e7`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
# Thu, 03 Oct 2024 17:49:34 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 03 Oct 2024 17:49:34 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 03 Oct 2024 17:49:34 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Thu, 03 Oct 2024 17:49:34 GMT
WORKDIR /tmp
# Thu, 03 Oct 2024 17:49:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e357e1f94476a03fde298261e8c007d487d3cfade45a9eef064eba724a5c5e2e`  
		Last Modified: Tue, 03 Dec 2024 01:30:26 GMT  
		Size: 52.2 MB (52245994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ddd5d354c274ecfcc46d65ee00d56e1c0ba724f5216dd62bef142f3831117a`  
		Last Modified: Tue, 03 Dec 2024 15:03:01 GMT  
		Size: 102.7 MB (102747753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e701fbe9b0a28ce175d3c6a046007f78a9ad59f3b89dc0e32297421d5837875c`  
		Last Modified: Tue, 03 Dec 2024 15:07:01 GMT  
		Size: 69.3 MB (69285960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ce4e751402750fddb6f13ce33260b940675ddb8a5639cf0aa16febbe898d12`  
		Last Modified: Tue, 03 Dec 2024 15:06:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:25f8564b04a518da1d919fcd2f01e4779f3e638e6070d45f9b93febad3a7b4e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7356399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39b1347e7061c700f0460566fa11c37eed314254cead02c2f18a6841d1ae473f`

```dockerfile
```

-	Layers:
	-	`sha256:f88eca09b41793cdc4096d99383ff76ddf4387c10d00c93b6cacd91eb0a7b9e1`  
		Last Modified: Tue, 03 Dec 2024 15:06:59 GMT  
		Size: 7.3 MB (7342039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e3d50087ad648bed53d1662cc0c7f0062bddd6d765534964dada0639c9e0a22`  
		Last Modified: Tue, 03 Dec 2024 15:06:58 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
