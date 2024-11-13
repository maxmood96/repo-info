## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:1af7745d0013b3af82ace5eb742c8b33a4dcc1a02ba26d92aabb4fa0d4a721b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:f16c3855779c036735fb32c981a86944a06c2d20899584a781ad2071d2b807d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263911209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db1288c756addd93a993629646f56a163d26991552f4ac9fae30290bb9ca86f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813885260b785c3dde8f3ab3d6a50cd54ff8b591801c56840809ad25f7759707`  
		Last Modified: Tue, 12 Nov 2024 02:50:14 GMT  
		Size: 165.3 MB (165295077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4da118a369f53a09cd86efc35d2b8e3ff25f57a39c6163c1f9a4edd3ec9af7`  
		Last Modified: Tue, 12 Nov 2024 02:50:13 GMT  
		Size: 69.5 MB (69487097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f6a5fbb7563819cf0a1acb10ebefd27227f4c2d82f8f2a23f9bd875a9fad89`  
		Last Modified: Tue, 12 Nov 2024 02:50:12 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26fd084c9a88aad844e59487dad1469de8cec368f4bc7f6c86501a31ddc32ee`  
		Last Modified: Tue, 12 Nov 2024 02:50:12 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:fc05a733fdee58dfda8b6f055889326a0644cbbc22e9c708a5b44aef0fe7d973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b9931bb09f7fec019331b964dc026037fb2f37fa4846e4309931b92ae6c3f5`

```dockerfile
```

-	Layers:
	-	`sha256:d959ade000cb6042349da0e55401f4349e3b9a702e5078d8250e2596929fb192`  
		Last Modified: Tue, 12 Nov 2024 02:50:12 GMT  
		Size: 4.9 MB (4925641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d156d00fbd3887ab2d2fbe8c8075626af5ac696458f4c4a46fe732992a88565`  
		Last Modified: Tue, 12 Nov 2024 02:50:12 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:99e903d71dddac6fc84892a5fbd5ae122f8be59e461c666c42d85c742cbaf9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261774806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6eb4901d8d0a6a44cbfdaa801539cc94b78a78131e1359459fdaf893d1e1453`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD rootfs.tar.xz / # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
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
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 03 Oct 2024 17:49:34 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 03 Oct 2024 17:49:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77c14864cf27b628705d7be5859bafc170f797758a7e42ae19772d2a2bc22b74`  
		Last Modified: Wed, 13 Nov 2024 01:34:33 GMT  
		Size: 163.3 MB (163281781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628a6062e6b53070deab6821c1aa3861e0c2fd5f3cd937af157e446b17702fba`  
		Last Modified: Wed, 13 Nov 2024 01:38:59 GMT  
		Size: 69.3 MB (69334629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10087b3d7f280d22cc51b182c6332044200ed1efdfd2d540eeb53dc02ae0fa8c`  
		Last Modified: Wed, 13 Nov 2024 01:38:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eabf15fe7d2a27689b98c73ccb9f53ea765361226b14cf47dfd061a88b6d1e7`  
		Last Modified: Wed, 13 Nov 2024 01:38:56 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cda760da2b4ddd3d8b6ce327ef60427f7f2b225852d0228668af49a23ff3d316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4945981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5385e7bc6d951a56ad97f08035cbef79c8f5a238580a23f9f97d0fb3e273d77`

```dockerfile
```

-	Layers:
	-	`sha256:5e014dfd648c6c5052ce467809c6ae8d3d974a4ecc8092e3b2c520f96561dc82`  
		Last Modified: Wed, 13 Nov 2024 01:38:57 GMT  
		Size: 4.9 MB (4930785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a122002ccec68fda1794ba9fe21633552758bbc4ccd7362ed79a086363c6f6f8`  
		Last Modified: Wed, 13 Nov 2024 01:38:56 GMT  
		Size: 15.2 KB (15196 bytes)  
		MIME: application/vnd.in-toto+json
