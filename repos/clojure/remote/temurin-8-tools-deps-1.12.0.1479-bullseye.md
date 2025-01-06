## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye`

```console
$ docker pull clojure@sha256:66ca71390cfba3d968a19fa26b2fcfee1a30489ac6b8d1c945996ce14a70dc02
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
$ docker pull clojure@sha256:8a3889de9cd178f7cde653d70a49abc9bb1df979e6388da923de7d2ad9421b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.3 MB (224279856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6078f7728ba47809054257ddcbbbee946f34a1f357743d3f986f7dd6e15cb4`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1734912000'
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
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Last Modified: Tue, 24 Dec 2024 21:34:37 GMT  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b800810d94f2437b1b4b09be721d9d61a975b92a33a41f099a3b069911fc2d7`  
		Last Modified: Wed, 25 Dec 2024 07:13:01 GMT  
		Size: 102.7 MB (102747715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf9a8398b69a922af0b2b7cc8bd2c36d72147aeaca3d0759530d64d9e57760b`  
		Last Modified: Wed, 25 Dec 2024 07:16:17 GMT  
		Size: 69.3 MB (69285798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5f324995788e452baa269833d0f30daaf9e4493aa5f421b1492c89d9951909`  
		Last Modified: Wed, 25 Dec 2024 07:16:14 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bbcac033593c24beaf8b5b587d75f6155495f52392ba7dc54f44734aff920d1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7346870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2e7acf10a1b8a875e0b5e4936328607b824b83c088e3ce717faf606209413a`

```dockerfile
```

-	Layers:
	-	`sha256:232f5400c110889365a60e3fc2d5e1cd028c06b0abe5f9dd5de0e1d87605947a`  
		Last Modified: Wed, 25 Dec 2024 07:16:15 GMT  
		Size: 7.3 MB (7332510 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d698650ec3ea6da32847c83bed65756b6bada232774746541d7bb4132f1aa6bc`  
		Last Modified: Wed, 25 Dec 2024 07:16:14 GMT  
		Size: 14.4 KB (14360 bytes)  
		MIME: application/vnd.in-toto+json
