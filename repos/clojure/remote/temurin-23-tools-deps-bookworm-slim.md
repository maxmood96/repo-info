## `clojure:temurin-23-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:b4d783214c41132d66a4c175f7c33a46f1a3b870250279e0f5fa5ff70faa1c13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; amd64

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

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

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

### `clojure:temurin-23-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:bbe56d215d5721414fa97ab7835228ab204f5234fad2cabbe1034d9abda8419c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.8 MB (261784300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65594f3895ed5e7341910f37e761c946c56c516e3a4f9b8adc5d0cba197b0511`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:702193928cded0bcec5edbf4a5660961e7caef8c9d9cafea3337b7f6720c4464 in / 
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
	-	`sha256:83d624c4be2db5b81ae220b6b10cbc9a559d5800fd32556f4020727098f71ed0`  
		Last Modified: Thu, 17 Oct 2024 01:14:39 GMT  
		Size: 29.2 MB (29156341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212b9739eb7b24a5ec2f5127e76d78d0c8e76e9b3625b0f4c4ac69eb55a208a2`  
		Last Modified: Thu, 24 Oct 2024 09:37:11 GMT  
		Size: 163.3 MB (163281781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10b27125eb2a31577d0f22bcb34ab16b1d22ef29b8ff60555f180ee705be161`  
		Last Modified: Thu, 24 Oct 2024 09:43:13 GMT  
		Size: 69.3 MB (69345137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9edc33e2164124cf30446fe1ecc2ef7c95fce48dd7e6af717513c8b7ff831c45`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd79a55c67bdb8ac1cbd0ecbfd21848cae119582507e331f3f6ea3e5b476f61b`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b133c43d42d23a95b44e03976c9dc17bdbe80aacfd69df68cd723f13ee4a43d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4946579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebad85d8a6ba9285644f495d14f6a8071e3db02ca1f2c0e202536a8d9eb290d3`

```dockerfile
```

-	Layers:
	-	`sha256:5068c6749041fb544b6ba9bf999d4ccd12c67f03fee3872fecb5a73f7e85673f`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 4.9 MB (4930749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b3906a2f380b718490acdc912986d00f2d5d87d78160a8aa7668ced188b3f5c`  
		Last Modified: Thu, 24 Oct 2024 09:43:11 GMT  
		Size: 15.8 KB (15830 bytes)  
		MIME: application/vnd.in-toto+json
