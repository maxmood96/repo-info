## `clojure:temurin-8-bullseye`

```console
$ docker pull clojure@sha256:5f0b04e26e919d68b553c396f461924cdc4d2c10048201ed9772cfe09fb76b0e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:4f1088ac618a6692e95fc2bcafe09b574272afea757b2e893e23c8ed5298541b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.5 MB (178534711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ae0c474d6087708bcc625720bf117f2943fd21f282815f9d154f50b49766d3`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:01:28 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:01:28 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:01:28 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:01:28 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:01:28 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:01:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:01:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:01:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ced3088fc7691915325d6187786ba346149f7c9dcdbfb3772ca71be74bf87622`  
		Last Modified: Tue, 07 Apr 2026 00:10:43 GMT  
		Size: 53.8 MB (53762793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb56e3bca0a6bbd7f74ee090019c6295875fab3c15fab8d6ec95335725792b`  
		Last Modified: Wed, 15 Apr 2026 22:02:01 GMT  
		Size: 55.2 MB (55170060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b3e96feda5f8d990ba196c55a389fe509dd1e9f58ddcb0ba52c5770cc88d3c`  
		Last Modified: Wed, 15 Apr 2026 22:02:02 GMT  
		Size: 69.6 MB (69601214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dd456a536c19c9d2b65f3d34ac7b8d12798effa6c6e8827f3bce12bb134520`  
		Last Modified: Wed, 15 Apr 2026 22:01:58 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:51429059fd4606ad9cf580fe1e2e5e65b194ab7a5038953ffe8b2c118f934428
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7542834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0182c4dc9836836da6f0f01c887dee670824e8b33d3925e54b04682a08cd7263`

```dockerfile
```

-	Layers:
	-	`sha256:66a06cbe4266dac984c3aa5975111968d3325a6a2b6d3e41fed361d6f61a0f90`  
		Last Modified: Wed, 15 Apr 2026 22:01:59 GMT  
		Size: 7.5 MB (7528640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f92573355178c3211e88a4d3eac3355c61cf905e36b77a2e808ae036807f614e`  
		Last Modified: Wed, 15 Apr 2026 22:01:59 GMT  
		Size: 14.2 KB (14194 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:50a6b9b7078dca86f0493501aa9eb70cff44f2dc0c491814c846e7e44709147c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.2 MB (176236267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:646ae34ce406c140d1757c6805aa4f72d38cc3a5bf2d99c30d31ca1dda032666`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1775433600'
# Wed, 15 Apr 2026 22:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 15 Apr 2026 22:13:02 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 15 Apr 2026 22:13:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:13:02 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Wed, 15 Apr 2026 22:13:02 GMT
WORKDIR /tmp
# Wed, 15 Apr 2026 22:13:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 15 Apr 2026 22:13:17 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 15 Apr 2026 22:13:17 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:910d955c4ed64a8ee0854ded27fe508086448dca2dcf21a0af023b8bc9d2020f`  
		Last Modified: Tue, 07 Apr 2026 00:10:48 GMT  
		Size: 52.2 MB (52247615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e619982beb6dd752917df921027c8aada90845912e439e959109180f11c516ee`  
		Last Modified: Wed, 15 Apr 2026 22:13:36 GMT  
		Size: 54.3 MB (54251614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675e134df14ccb92407b28ebe7eebb352c52a4a52c2117d7aa1ce3951634eede`  
		Last Modified: Wed, 15 Apr 2026 22:13:37 GMT  
		Size: 69.7 MB (69736392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760e8444c020d5fb5c731ed41d2d0bf003de112570d2e8f1b4a1d959bed215d5`  
		Last Modified: Wed, 15 Apr 2026 22:13:33 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:0c83019e420e804fec0ee791da9bac7a2e15c85a3d7f21a8ab9c56d2db8e487f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7548751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b04189c37c994222bf833d65a3f64882a86049b92bb9fd7995f806b358387`

```dockerfile
```

-	Layers:
	-	`sha256:7ca592ddaba33399d2729e6b9ee36891748b918402ec4a224dca6729c2dcfbf7`  
		Last Modified: Wed, 15 Apr 2026 22:13:34 GMT  
		Size: 7.5 MB (7534439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb353eedd0d00808533ceff5ad194f7d471e12aaa0ca12ed7431f7fcced264b2`  
		Last Modified: Wed, 15 Apr 2026 22:13:33 GMT  
		Size: 14.3 KB (14312 bytes)  
		MIME: application/vnd.in-toto+json
