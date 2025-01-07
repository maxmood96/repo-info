## `clojure:temurin-23-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:752297afecfa5f4e1c97ebc5791c8ea9ccd40a520f9d7d725b066feb018d3d5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ea509773b68e9f8642d044d36f369ed44b32176fe918de8b9ee357a71330e334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.2 MB (288213287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4042f81352f17c9923092d8d5298eaeccac1e41fe24d8a769af9d8028b7c07`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Mon, 06 Jan 2025 23:07:46 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 06 Jan 2025 23:07:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5d6e107a26c2ffb6e234f04132358dea70a691a64c1152f984d2f2ba0e218c58`  
		Size: 53.7 MB (53738957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d02615de9f4b20698c00a42c3fbb38ac91a055cdd96d08162cca722ada6f7d`  
		Last Modified: Tue, 07 Jan 2025 02:29:34 GMT  
		Size: 165.3 MB (165295090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47d10ef4226e2120eeefd9f6692b831dfdf541c8d4eef2523704d02ecc68c7aa`  
		Last Modified: Tue, 07 Jan 2025 02:29:33 GMT  
		Size: 69.2 MB (69178203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273cc6dc050f63b620ea842265adc6e1c786d5d984a1c64f6c24759df3525110`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed1f86d63e58969ecf8736ad617bc2f8ccaf577498c79422c8e276f23cfa9f8`  
		Last Modified: Tue, 07 Jan 2025 02:29:31 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:4cff475c00f0eec94ea33b682485127c725dcec2d64f8d5449038e51040d7daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7225382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7eaf088837a0c71a8d0d6a212b2413fa5f8ad95f7c74a1e62c02a0061e2d38`

```dockerfile
```

-	Layers:
	-	`sha256:e64a2beb25adb5ef070884cb21dbfd3f2be88f36af72ac8772992e279b8d3639`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 7.2 MB (7209562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7521eb1c730cb8c9316ea4e3815b85022a638a9a2f9748c06f7183046101f262`  
		Last Modified: Tue, 07 Jan 2025 02:29:32 GMT  
		Size: 15.8 KB (15820 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:aa97a7e816a07cc80cfe67ad856fb66e1c48ad9c404d4fdde934f30eea5fcc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284814332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bb49171d39cddf713503eab03e866ce2560f064f0a4f444aa7b1a7545a53c2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:447d428f9ffe60c6c8cc59e00901cd865a36737372ba05710598d7eaf0a1144d`  
		Size: 52.2 MB (52245698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6695db2a9af9c621e2afd751a22f972795b62d6695e9f4d372982636e107ce9`  
		Last Modified: Wed, 25 Dec 2024 07:38:55 GMT  
		Size: 163.3 MB (163281797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d588326635de5735f25ba3e4bd1c362a537d18c406d156470851a243421ab01`  
		Last Modified: Wed, 25 Dec 2024 07:42:06 GMT  
		Size: 69.3 MB (69285798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e5d76eac561e7b607a61d7430c9f32dc2e7c878eb7e5e5db8496fc5aa197f`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebebd1c0d2ce3c4335b106d0636d51b5a4ea94aba0c6fdff2d2d74a2a77fd077`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:78fe273dfaf33e789e6706af0a0ee8e3db36358daad58349229804b955853875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7229915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70851bd9ff73e21d401c42826ca0a6f339319cbe3e5d4d8cae1ce180e8289642`

```dockerfile
```

-	Layers:
	-	`sha256:205b5820aa9271a6cfc0b4aaeb5ca197520196d4325e252d280ef503ac93de27`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 7.2 MB (7213978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c251eb4cdbb66475d5ea946abcbd044655257cadc45cda2da22b654033de1c43`  
		Last Modified: Wed, 25 Dec 2024 07:42:04 GMT  
		Size: 15.9 KB (15937 bytes)  
		MIME: application/vnd.in-toto+json
