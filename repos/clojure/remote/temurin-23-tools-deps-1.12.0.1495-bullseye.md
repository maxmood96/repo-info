## `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye`

```console
$ docker pull clojure@sha256:9d7e0e803fa059da94ba051a8fdd5ec7de5bbedfaecc9331a2b9a1eda9d29849
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye` - linux; amd64

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

### `clojure:temurin-23-tools-deps-1.12.0.1495-bullseye` - unknown; unknown

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
