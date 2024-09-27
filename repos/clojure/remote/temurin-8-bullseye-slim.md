## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:972a1111627a67c5c590f25bac12b3856450776cf318c833e8fe2658ff062b0a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7714183680b0be7e929aecfff24147fd5f4ab6d097a146c07e2fd253a02f421b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 MB (193981202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245869dcd429cfa7cebac57a64051722640dc4627f67a9fc54fff976dbcad2a1`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207c2ba6649b55962f49a9654e8eec555dd20620c00939c426a643b530a12fb5`  
		Last Modified: Fri, 27 Sep 2024 06:01:03 GMT  
		Size: 103.6 MB (103611881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf82cc4305cad25f17887eeafb7211fecff533a0686015af65237e1b44521fa`  
		Last Modified: Fri, 27 Sep 2024 06:01:02 GMT  
		Size: 58.9 MB (58940079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626791723e83d46e4e149b93d892c7aab99bf657e63a1e7ac3882899e1b87260`  
		Last Modified: Fri, 27 Sep 2024 06:01:01 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d8ef9f797d668db58378ae5d2db920c71411bb68a098d8a4ede6a0dab8f292e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423aadbd7426420207a19e816095486088ddc7f4f9ba0287ed473dc3cb867024`

```dockerfile
```

-	Layers:
	-	`sha256:02f2efa6689435394dd112d7a87e6f2cb55e40e7e5197809d82ee842e41f49d1`  
		Last Modified: Fri, 27 Sep 2024 06:01:02 GMT  
		Size: 5.2 MB (5221615 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f15225f555f066fe71358a35b31ba814ca8bdd41ee6385aa186cb4fe674c242`  
		Last Modified: Fri, 27 Sep 2024 06:01:01 GMT  
		Size: 13.9 KB (13920 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75c7d506d6d8ea57c65a8cdeae4d69813810574e536eb69fd797f0a40708e6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.9 MB (191877744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5c1e5b891c4fb5f9379f73aabccd0898307d0738646d97465ac4cbc181f9fe`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 06 Sep 2024 16:59:26 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["bash"]
# Fri, 06 Sep 2024 16:59:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 06 Sep 2024 16:59:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 06 Sep 2024 16:59:26 GMT
ENV CLOJURE_VERSION=1.12.0.1479
# Fri, 06 Sep 2024 16:59:26 GMT
WORKDIR /tmp
# Fri, 06 Sep 2024 16:59:26 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "94f29b9b66183bd58307c46fb561fd9e9148666bac13a4518a9931b6f989d830 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 06 Sep 2024 16:59:26 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3f6e981127df7da95100e4aac7e6941cd3b2f47348a54ecf887866671faced`  
		Last Modified: Fri, 27 Sep 2024 10:18:50 GMT  
		Size: 102.7 MB (102729229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbe145198ca46d1cc53a591bba3135621fc6290b2963092e8fd9a635d0021bf`  
		Last Modified: Fri, 27 Sep 2024 10:22:12 GMT  
		Size: 59.1 MB (59072714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc819fa428e26cf1179525a72880251a1ff6ad0ac82c5feb6e0af6d70cd10767`  
		Last Modified: Fri, 27 Sep 2024 10:22:07 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:d64b352d5939e08c6b3a1262993a756403238338395f3bf7bceab869fe2155ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5242511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65b9421a0e0e07551baef96b20921695855679c5598dd0a682a16459c0e9c9dd`

```dockerfile
```

-	Layers:
	-	`sha256:7ecdecd3363a2deae106dc9e090869ea13c8e1c7f5b81b937af17f9781b65a78`  
		Last Modified: Fri, 27 Sep 2024 10:22:07 GMT  
		Size: 5.2 MB (5228051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a174bab63d87d65c2792e8250f6b4e0a33f33e7ce308767fdd4023eeee166ac`  
		Last Modified: Fri, 27 Sep 2024 10:22:06 GMT  
		Size: 14.5 KB (14460 bytes)  
		MIME: application/vnd.in-toto+json
