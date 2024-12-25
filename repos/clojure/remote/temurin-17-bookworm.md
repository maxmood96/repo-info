## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:35b27062ba566b62d0a617142083b8e5974b96fd40bc9fc9c9d9d21600a0cdf6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:d662635b960349360b73dc081ddf79eef25f4dbdcb5ef21e10be1243724cd5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.8 MB (273779192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f276d76a60ebf3c427b319318bd4b5b159e06f1e0254ab5c3d4a78237daac876`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05aaf630c4ced92c4d0f62cdcbee20563bf8665f5d4c5109c0665de94dc2b5d`  
		Last Modified: Tue, 24 Dec 2024 22:38:17 GMT  
		Size: 144.5 MB (144536708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0cd88d471f3301e4b23e457d41820589f85113bf3baeab6066ad00ee5041c9`  
		Last Modified: Tue, 24 Dec 2024 22:38:16 GMT  
		Size: 80.7 MB (80744376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5270bf8bb2d67a07f4d0c01469a7976e8b2b7a61b4bb240f83e0663ceb03802`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531d487085302fbd21f6043916c9b20081b98c4eeecd1beda5e3db9d36e67705`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:cc6da30e0a3be1670ff6d13d94f3e44770ceae0281ba70888786462de9fcdd12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7186839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af4aeb7f0041e6457bc0248fff9f27343aa798ebbfa1cfec21bda41a76441bf8`

```dockerfile
```

-	Layers:
	-	`sha256:464fd0ffb6a81a1f5a1418ce62f9d1953680f7e4097b11629c03172e35bd954d`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
		Size: 7.2 MB (7171018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e94b07fcf79cf88f6222a25f24697d75dfede67795a47f29ce8d7bb987b6c3e`  
		Last Modified: Tue, 24 Dec 2024 22:38:15 GMT  
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
