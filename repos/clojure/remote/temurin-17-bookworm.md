## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:a2839b18f51a8173a19d645a5feefd7659ea5cbbda79512a3dba4f97834802d5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:db44f4604181a8a7d913d2877abe3d3bb93c0447a06bd0026fbcec5f3fbb23bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273779253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d3ee58326d5aef8d0699334f3f333f621bfcbd480f538f8ae833f3569238019`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6632396ef0a08ffe4b0540ef89c7c724dec17caf753123eb5ff78eaf38e7a0`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 144.5 MB (144536676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26e0c85b478c728185beca6f4656ed8f9d4ce104e903910d33d394d521029f8`  
		Last Modified: Tue, 03 Dec 2024 03:19:54 GMT  
		Size: 80.7 MB (80744326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b9c819bf1b51ad08d227668122eb7519ed9409b6c8806cc8084d850fe4c18f`  
		Last Modified: Tue, 03 Dec 2024 03:19:52 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7c92f678237d1a51d71f02ffe06251fab4cccd28be90b7ddf0589ba376b04`  
		Last Modified: Tue, 03 Dec 2024 03:19:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:51d01fdc1f7e88387e9764a3e0be21a96942f29a6cfeccb428f87414257a0c87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7196996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cee9ae990a0cad00dc2a1c3a8ccd88a66ab3d0a31a50790eac99a5862036d91`

```dockerfile
```

-	Layers:
	-	`sha256:e1dd5417d7cc820f8d2abdbbe21ea16bd217ad000b1623716cf1115ca6f4eb7c`  
		Last Modified: Tue, 03 Dec 2024 03:19:53 GMT  
		Size: 7.2 MB (7181175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc8e6a2b93b1885e7bd0eb8e36c28927d2dc27b20bcc6552e58692bb794c3955`  
		Last Modified: Tue, 03 Dec 2024 03:19:52 GMT  
		Size: 15.8 KB (15821 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6182b006ad0f1884e2a23f0afd336bc24e15a6dc069046be4b4458d133e03dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272293550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac61fb50f7ec6e6ab9647337db5df175c16e2c6071166d713627523096706875`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
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
	-	`sha256:82312fccb35f18983647c1ea71154b98ae9893fb61ca4febe12d584a3ea9ad6d`  
		Last Modified: Tue, 03 Dec 2024 01:29:57 GMT  
		Size: 48.3 MB (48325680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed142d0c0ce11607a436c5b2bc10b6dbe1e2f19b8ed3c8ff355d42ea3ea54749`  
		Last Modified: Tue, 03 Dec 2024 15:16:40 GMT  
		Size: 143.4 MB (143361009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86239b38ad75e81cc778156a1febec3d706d7de1af0a44443a10e41387fc33f`  
		Last Modified: Tue, 03 Dec 2024 15:21:02 GMT  
		Size: 80.6 MB (80605819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4631b242f4a6cb6ad6ff615ff7deb21e116463b4e3bc565931ba4d487bc4ac`  
		Last Modified: Tue, 03 Dec 2024 15:20:59 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0431e8ddd3d2f21e3265ff4995d8bffcb800ab9e96f10ccc4f7aa0fa6b8de1a7`  
		Last Modified: Tue, 03 Dec 2024 15:20:59 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cc034695b76678bd4dbb0708d9fe57054407bd8e55d8f65daea149e2357a3d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7202882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e799d7f2d5e3868e01dc999b441175335a3ccf2228616133ba14d04c69e3b94`

```dockerfile
```

-	Layers:
	-	`sha256:613c972a7430016bcfafb6b8106de7889050ea05f72c8e013c0ed3a20af56588`  
		Last Modified: Tue, 03 Dec 2024 15:21:00 GMT  
		Size: 7.2 MB (7186943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3b9829ac0d5a181f25370826a3dd60acc2bd57070dce707258f1c13f8d8563f`  
		Last Modified: Tue, 03 Dec 2024 15:20:59 GMT  
		Size: 15.9 KB (15939 bytes)  
		MIME: application/vnd.in-toto+json
