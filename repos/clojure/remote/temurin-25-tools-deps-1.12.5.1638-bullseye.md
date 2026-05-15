## `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye`

```console
$ docker pull clojure@sha256:2475d0d174aec59545c0f29544d721bf56c32536934cdb089d25d75148ae6a96
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:80236ca885e5c3255bcb70d4877d31d203383079ac54effc9685613d222d379f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.0 MB (215963164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d46eb0a93f30f5d7bb8f3e9a4939a353a61d76b4914fad37310f180f609916d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:36:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:26 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:26 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:26 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:39 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:39 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1c662d8f6b122c4f09d6ae1b210df55a5ba6e7b529807c0757ccba0c1ac508e0`  
		Last Modified: Fri, 08 May 2026 18:23:06 GMT  
		Size: 53.8 MB (53763343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15200dc3953865b4c94a26521e414ad5e38ca5e99a7c786261588a54ea68d6c`  
		Last Modified: Thu, 14 May 2026 23:37:01 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c732dc4a31ddb4ffa0acbf8b95c1c669f2f0c534ba43a35dd012b1350dd78844`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 69.6 MB (69624187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4009e87527a03248db8ec90c2e06548c8c3ed1dcc7fbb808e55273f1efea3031`  
		Last Modified: Thu, 14 May 2026 23:36:57 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a06ebdeb06692a7a1488e833a7bc91f8393199706aa5fc1e795b13c3e57ee0`  
		Last Modified: Thu, 14 May 2026 23:36:57 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:734c87cb867a63005586437b6ac50e02ac1b11e51947ea0d76c29e877a580023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7392949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98d5c3d672e3f589a3a01cf8cffc6fd61b4342497ad2629e01b3a429eebc6839`

```dockerfile
```

-	Layers:
	-	`sha256:c45300d0fdcf2a1e55b5741885815984cca4a14a224de3e443800e952ab93f3e`  
		Last Modified: Thu, 14 May 2026 23:36:58 GMT  
		Size: 7.4 MB (7376348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be5740dd52b67b1dd8bd73e05adee16d72ba2d8c5081c33a2b5d4ad0f5a56863`  
		Last Modified: Thu, 14 May 2026 23:36:57 GMT  
		Size: 16.6 KB (16601 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7af0546adfe4cfa63be8c4fe14df2edd79d7f562a5f758fa20c52ee82934182d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.6 MB (213560759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e512cd47bd83fcedf564da288d00431e723c1960a8ae243abccce26ae84b5ad`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:36:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:32 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:32 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:45 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:45 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:45 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:965b6eb1fb4a74ed46e659c8fd725e1bec9bed6684b59cbca85e48b6c25a32c6`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 52.3 MB (52253210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:187eb08a6f846fb3e763929b48e30d0d7619cc0e95f1146ae21a29d88b1a6619`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 91.5 MB (91542245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e9d61c2b104eb00feb9db14bcf33bf67e159867604c39a45853a7ccbc173c6`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 69.8 MB (69764258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f0be9d85b33c9a6abd5838e4fc725a22b68b27899414fddafe1654eb526757`  
		Last Modified: Thu, 14 May 2026 23:37:03 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e60dc6e8c3d4d6bc779cc0ef0986f11fda1287bdd5cfd25a3477cbc83e80bbd0`  
		Last Modified: Thu, 14 May 2026 23:37:03 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:125c642e0e4d0e810594f609fecb065c4766ffdbb716f23449940eefd0505c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670c67c205f1c70810ef66b4ef6fb2174302483586a566d015ee5db7f95aba7a`

```dockerfile
```

-	Layers:
	-	`sha256:260886ed397f38ea97e75accf83cbffad3e739308902b36a3bb3da3518b5f147`  
		Last Modified: Thu, 14 May 2026 23:37:03 GMT  
		Size: 7.4 MB (7381468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20f9d94c3e915d35d05e9c0093fbef362a90085198ee075b0655338ac754c569`  
		Last Modified: Thu, 14 May 2026 23:37:03 GMT  
		Size: 16.7 KB (16742 bytes)  
		MIME: application/vnd.in-toto+json
