## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:fddd15ca5baf1d1efccf89fd42326efc9443f862607cfb09c23e9859b22fad4c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:a65d473dcc5c47e0365330f47b8707146803633a06584786f8e18a374df35ef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.9 MB (235919298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e01b5f63821319fee1e30d3b7d2eb941f2b0f02679782ee348fbfcc8a289a39`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
CMD ["bash"]
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab49237006406e9b7ac3abc8904c975a5130df861c6ec73dbe2dd690ea61b34`  
		Last Modified: Sat, 12 Oct 2024 00:53:40 GMT  
		Size: 145.5 MB (145549934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21eaf38ee690092c4693c37bf95dbcb12c69c7b0907446a2c1fff5cfcc489d98`  
		Last Modified: Sat, 12 Oct 2024 00:53:39 GMT  
		Size: 58.9 MB (58940119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528ab99d513a5b597cacdb9bf934522b76bc1e49f0d328104500a7a3ef4ab70c`  
		Last Modified: Sat, 12 Oct 2024 00:53:38 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:755c24b80ffcab34c9ef20e7cbcd13130d13aa768cfc903e95df1e3708c7cdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5133628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a7a746ca9464d93b071de69ea0ec6e44520426dbc2a6e50e2a827677e04c76`

```dockerfile
```

-	Layers:
	-	`sha256:f3df967d5ca243e5efb79afae4685bd20856afd6ee24ce3b86c2d7e92f62cdba`  
		Last Modified: Sat, 12 Oct 2024 00:53:38 GMT  
		Size: 5.1 MB (5119652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eea9af78386fdc0e1d51d428e7330dd38b1d6a8ff5ba3037f3c3d2e3b7335d88`  
		Last Modified: Sat, 12 Oct 2024 00:53:38 GMT  
		Size: 14.0 KB (13976 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:94ff54174618b5562fa7cd585a788427949032885f25d877a6b9bb3cf77ebbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231504305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d1b7a483543f0413a631bf3a55cae92c52f4758e606933eebaf949b368a73fe`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
CMD ["bash"]
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33771f245d60b4ba877a7fcdcfef422da7796464ee121d48fd7a3fa7b21189d`  
		Last Modified: Sat, 12 Oct 2024 01:07:47 GMT  
		Size: 142.4 MB (142355083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29d8580f5ca08a5cf3ff63b837b0bca1c7ade4f0491c38d2305e3fba797c69b`  
		Last Modified: Sat, 12 Oct 2024 01:11:44 GMT  
		Size: 59.1 MB (59073417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d4fc30fe2871c4ca70cdca8ad6eafa4762d471d4c5faa6fde5f4d1d235d21c`  
		Last Modified: Sat, 12 Oct 2024 01:11:42 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:47fa003cc5345e8ee3061ff363f6bef40af1684f2bd5a3eb2a87350de4031f36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5140090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:757a4f7c325283b58f427f382db8c322f7e564ee35b68b1fd0938a9ee94a283e`

```dockerfile
```

-	Layers:
	-	`sha256:60d9720d8bc2f82aa5774b15de692e3d3dcf153243e29c0e6db05b9c2429ba49`  
		Last Modified: Sat, 12 Oct 2024 01:11:42 GMT  
		Size: 5.1 MB (5126008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5751b102b9d87037a5fe1220779656b8c0e19f7758fd69ede43a25f6768d65d`  
		Last Modified: Sat, 12 Oct 2024 01:11:42 GMT  
		Size: 14.1 KB (14082 bytes)  
		MIME: application/vnd.in-toto+json
