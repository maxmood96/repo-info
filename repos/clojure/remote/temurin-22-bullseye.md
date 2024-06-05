## `clojure:temurin-22-bullseye`

```console
$ docker pull clojure@sha256:97de387225bfd7120fa251ff0441b3c11c33a4642b4276d63d922baf41eb13f6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:3f37c0c0bd8b07736b0707e1c5f9a38b3404c566bdb2e3fbb5657d0857b14302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.6 MB (280631765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e376b3e62a63fec114dd4dc883a8a48117399bd4db0f41a0a6c29da51c180a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aeadfe8f8136fe6859d72a485d51436a20ac5a06e9b8ebdc150c19bcfa7167f`  
		Last Modified: Wed, 05 Jun 2024 06:12:43 GMT  
		Size: 156.7 MB (156715489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3140fb1ab11d5d70b9d313e1c8e9610914f30985ac1294fa240a2d1d173f2939`  
		Last Modified: Wed, 05 Jun 2024 06:12:42 GMT  
		Size: 68.8 MB (68815832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cefcca7185bbf7e957f60ec0812b90cbb6542f2ddc9e9e655b514a3d777eb8`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12926e4872f741af47533a774b1bc2612908c384b8218b6379ae4f18c0b4d101`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:bcf528b2389b91d8c1a499314dc2a66d1e761603faa4071764a7433a6c00a581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7015135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f5514d19de957a13b5749ed277298e8653833d8abc056d909356a79f0bbc7c`

```dockerfile
```

-	Layers:
	-	`sha256:149f1ec1c89b2676f67b7a85cc7aac6ebfe1ad902f356dffe1167eefc59611cb`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 7.0 MB (6999745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f8235b85f63d71e450e1feded126c0f0a3086aef0f52eb632e7904fc8bc5ae5`  
		Last Modified: Wed, 05 Jun 2024 06:12:41 GMT  
		Size: 15.4 KB (15390 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:235e49c7f9d2ba1b560fde7ae67e8c5565fb1e2d5d440f26967e953ce9341ab1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277407333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b2d48dd60020631d24ec2e40d7238f5d063d909fbcd3a2327d0db7d58adde0a`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 14 May 2024 00:39:47 GMT
ADD file:43721c605da3f74f0c3f71384780fc0e57e2478b88197672caaf4baa3eddab23 in / 
# Tue, 14 May 2024 00:39:48 GMT
CMD ["bash"]
# Tue, 28 May 2024 15:17:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 28 May 2024 15:17:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 May 2024 15:17:11 GMT
ENV CLOJURE_VERSION=1.11.3.1456
# Tue, 28 May 2024 15:17:11 GMT
WORKDIR /tmp
# Tue, 28 May 2024 15:17:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2f5edc801133c72a49e990816b0e245beb8b4e35a85524b4dd0b3fa03a4a5365 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 28 May 2024 15:17:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Tue, 28 May 2024 15:17:11 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 28 May 2024 15:17:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:078d9526cc72763b2db16388f6b511c18a73e3e7f9d229364b3b85a6b5277bc8`  
		Last Modified: Tue, 14 May 2024 00:43:13 GMT  
		Size: 53.7 MB (53738990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b506fec67212247201aaef56a3e9aa1d0f72e6019eaf9406f4e1594154828a9`  
		Last Modified: Wed, 05 Jun 2024 14:21:24 GMT  
		Size: 154.7 MB (154737997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a51a3b2ed64cde981af7a3aef6820a720b6bc376d23c5b11b62395af2735422`  
		Last Modified: Wed, 05 Jun 2024 14:26:22 GMT  
		Size: 68.9 MB (68929301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da859ff0b6e909d4dfae5d2db21d0971867bfd9b0ac0ef76d207836e7bfd6660`  
		Last Modified: Wed, 05 Jun 2024 14:26:19 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddc995a0862cb3cd0160f7acd7d9a5d58eed25a1529b360c36b2bc02a475341`  
		Last Modified: Wed, 05 Jun 2024 14:26:19 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2c016632a25dd21e5b28b89687c0717528286fe89fa3c955860120db82d270bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad3e0f8fb19f70cde6c2c09cf0a94cf0a23c4fb10ef3ef8fb82dec65e5c726f`

```dockerfile
```

-	Layers:
	-	`sha256:8beb8c25ac42b589040f8557f3ed7906cc85beb04c8e27bda32a5c47f585bbd1`  
		Last Modified: Wed, 05 Jun 2024 14:26:20 GMT  
		Size: 7.0 MB (7005467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375a85eed17a937f5e0111879f85f96cb4fcc010e9ce1c1da871a4fd2cac83be`  
		Last Modified: Wed, 05 Jun 2024 14:26:20 GMT  
		Size: 15.9 KB (15926 bytes)  
		MIME: application/vnd.in-toto+json
