## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:6b142caa49df80480f7388493b48ddcd0ec6497fae964ab8c2990a0ba0438295
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ddeaa60bb9f03e43ad7ac5cf09a1ac68538dc19debb38fb9db253563bee6e3da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242276342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e97b524e9f872d577bc0dc46d49119fc696b730c9a541ad99c34f338a66fd1af`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 06 Jan 2025 23:07:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8242f423d75ebf7f76848baef3eeece481a8be52508eaf61d0e6ad887cdea4ad`  
		Last Modified: Tue, 14 Jan 2025 02:44:25 GMT  
		Size: 144.5 MB (144536716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b893d86fd0f744766b026034c97987978224246e6b49819ba47b97228c7bcca`  
		Last Modified: Tue, 14 Jan 2025 02:44:24 GMT  
		Size: 69.5 MB (69526169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f3d7f74309cf3a5d7eb685fe8c7511d53f1959d2800e6ce2184d94ca051500`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:747740e0b6ffda8c6b55f8c897a803238d5bb71e0ffd99895d956315aa82e575`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:527afdfb1ec1bbd2e3d8c5f96096ee4fece79351d83ddeada301f2c85b3c15fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c9c5defbe1af76e62dc4dea71713a18d23ece41f46641aa9fef4ce12589998`

```dockerfile
```

-	Layers:
	-	`sha256:2aa17920785b6cfc1bf74b64b8f2846d7e6c978d9e681afc81fcab0982398b05`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 4.9 MB (4912569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42f244aa73fd4ec355f1786bde140ab5b72d6ec5d634e4278f006e1b564f88ff`  
		Last Modified: Tue, 14 Jan 2025 02:44:23 GMT  
		Size: 15.9 KB (15878 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:37e2ac9fcc60ce956fa04561bfccf297f62e1d4765d5bc3618e27722aa7d7535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.6 MB (240590859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e621fdbd32e0347c2752fafa7190209ac79244d7ee274f6230b59cba63fee`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 23 Dec 2024 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b09e1a9dd798a45459f926ad8d2252d7874c16b30997fd9b3909132732a599`  
		Last Modified: Wed, 25 Dec 2024 07:25:32 GMT  
		Size: 143.4 MB (143360951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa51f3fc1e3c396528855d0c45f3f14128d697fb80552eed9d6bcdf059f80545`  
		Last Modified: Tue, 07 Jan 2025 03:27:45 GMT  
		Size: 69.2 MB (69170146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c209260cba2b81d679130785391d6b78aac96568a2032bf14e96754279e5c8f`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d54a7d877f882e31c5a97409e7bb3e57be0f39c93adc61f54cb756228cc0f4`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7392dcb8281c53aabbcbbba412164c99776f857c320f199eb631a904e522b191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce7afaca4f9526b7a61bc84a4cfe7b38634e2c61164fdbaf8214b3c49c98a7f9`

```dockerfile
```

-	Layers:
	-	`sha256:1fad92dddcbfbf896b728310526df19aacb8f55c47486157401eba287d1ee50d`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 4.9 MB (4918330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1e474f4c36005a7c33158568a2a2ba9ab829b1dd1bcd1890a1bc3f878b31ef`  
		Last Modified: Tue, 07 Jan 2025 03:27:42 GMT  
		Size: 16.0 KB (15997 bytes)  
		MIME: application/vnd.in-toto+json
