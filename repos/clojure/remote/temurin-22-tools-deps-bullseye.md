## `clojure:temurin-22-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:5cc8c8aaed443e69bb22c4f9b9d9adbcba7029616ee9abf54646df94e2b74f1e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bullseye` - linux; amd64

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

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

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

### `clojure:temurin-22-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:69ac6dd673c6cdac6784807c1ce6adeea8ff9e4998599b08b0836a16f03a94ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277407675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51f03b70dda7dbc7a5cfff3efed017a7bbf5edf37dc924291248dc8f03d43a7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 28 May 2024 15:17:11 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Tue, 28 May 2024 15:17:11 GMT
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
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d963a96394e2a9f4df474372727ed0b58c4b095d7c668d6d92d142be8c953f6a`  
		Last Modified: Thu, 13 Jun 2024 12:01:27 GMT  
		Size: 154.7 MB (154738000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2326b0c8327e1c12f1d945ce82bdfc15a6a63ec380d731fbd8bd97eac0ecc17a`  
		Last Modified: Thu, 13 Jun 2024 12:04:48 GMT  
		Size: 68.9 MB (68929046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebc58e1f7350a38d4948317a9ead896de7164e1a067d7749231196af56ba52a`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75600f3cbe00f39734bca9007d468e47515e0fd217ffce6a600535efc0284e8`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c3b1c49ea70e0d0b3ee3d4617c2ddf5ab41b30401fe63d49fa32ca7e5f0978f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7021442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32164dd92e21ffd462033307c7417d1e222d47e8572b6c060f43fedcb3b6fa1`

```dockerfile
```

-	Layers:
	-	`sha256:8a522f64a78a9681f717e9702d51a9fa56e35c296cf45b7f3e4f54716e935f74`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 7.0 MB (7005467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87f433b709a9900fbc8ebcfe5628182f81d489ccbaa3724212312d7f7d4fd7ee`  
		Last Modified: Thu, 13 Jun 2024 12:04:46 GMT  
		Size: 16.0 KB (15975 bytes)  
		MIME: application/vnd.in-toto+json
