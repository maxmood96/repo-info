## `clojure:temurin-11-bullseye`

```console
$ docker pull clojure@sha256:e421952e3a6ca05bc6cb3988715d8b1d84f6d15a5a8b6dddf60506000b3e05ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:2aead5489dd05aa9e2b4836afc9cff8d2480af84895848d156fc80a5f9578310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268519631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4518094aae1e01f9a1d52f70606c61f99eedfdd753ff78a4b4aa7a84652bcd`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1734912000'
# Mon, 06 Jan 2025 23:07:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 06 Jan 2025 23:07:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 06 Jan 2025 23:07:46 GMT
ENV CLOJURE_VERSION=1.12.0.1495
# Mon, 06 Jan 2025 23:07:46 GMT
WORKDIR /tmp
# Mon, 06 Jan 2025 23:07:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8408034c095c531155acb08bef65ad1edf25f55226bb086dfaf0d0eee9cadd59 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030b19a1def526ce102fd9bf80b1804a4bdfa2bafa721151475c07907444fda4`  
		Last Modified: Tue, 07 Jan 2025 02:29:37 GMT  
		Size: 145.6 MB (145601480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8d8ae6bd2fc3de43a6cfa6035800451c6999f9838bdfbbfce3f190d5012d535`  
		Last Modified: Tue, 07 Jan 2025 02:29:33 GMT  
		Size: 69.2 MB (69178549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6240d0775ef20f3fe07d392f9b7c06fe5e0395bd59e08c088448efcc34c04c94`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:6b284bfabcecab9a06275947713dd6dcb1ab16ffa7c8eb7c83f7df4e5ddd17d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7238948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9804d3bcb90239f57cba6ee1ae88a6cdbb61ea856ee9edb2fb7a3bcb932ea2`

```dockerfile
```

-	Layers:
	-	`sha256:92df9fa3615a51dd1cf2593f0b3ce0dff239f7df1ba4f6c3273646c74f8a76b1`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 7.2 MB (7224696 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:154945c0eae3c18cdddfe27ca3cd83692d7a2ea429f060238bb050a1996d85c0`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 14.3 KB (14252 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:836fb7bb9ba2f94c59f9e15f7d88cf71b6da5ac76e1f380739db2ca9d107e70b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263921251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55c72e0700816276a3c0220e4632677f76a72816a92a35cad77eda7231e9cd79`
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
	-	`sha256:ac580959112f2958e7f4b4eb9b360444b899d195029d8e7b71a031c4435f09e7`  
		Last Modified: Wed, 25 Dec 2024 07:20:01 GMT  
		Size: 142.4 MB (142388995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43c897ab17d6be4d7f6bf7714dba38b3159350ef91bc30ae4bf3b90458c5358`  
		Size: 69.3 MB (69285915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67480591efe92e9825bd54646f112cc8f6ae0a4e2ccc0df7a3974842f2ab5f05`  
		Last Modified: Wed, 25 Dec 2024 07:22:57 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:fad4c537d8c45a89adcc07fed7a49a07c6fd2b4308ba6beb743125675a1c0fb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7244721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e9769423f5d0ef232c08e5eb40e7470bb3d27052f272885f5a0895814da8e3`

```dockerfile
```

-	Layers:
	-	`sha256:c400c007b2f7474d620d9c5f96430be9d1b3e7459835974e4f3b592aa4338ec9`  
		Last Modified: Wed, 25 Dec 2024 07:22:58 GMT  
		Size: 7.2 MB (7230351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff45cff8a509ae25d2eb4ee91da26e031b77407304444074dff7b4c723df5931`  
		Last Modified: Wed, 25 Dec 2024 07:22:57 GMT  
		Size: 14.4 KB (14370 bytes)  
		MIME: application/vnd.in-toto+json
