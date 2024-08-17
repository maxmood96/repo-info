## `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim`

```console
$ docker pull clojure@sha256:2e4063f1a0363d3be03ad8cf264db0bc551b1b8d1c2cc30fae4ed65348d39f7a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d05900492f7e4c3d5082b28eb8226422ea22ee186bfbddb79c0eaf6b0c4b0218
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.7 MB (243700888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb245f87a4eabad217f12c72ed8ce4165fc48afc8d8fce16422cf6eee8024bcb`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:3d9897cfe027ecc7cbdb16e74a676ed143725ea2d08dbb0dde23309e041de0f3 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e4fff0779e6ddd22366469f08626c3ab1884b5cbe1719b26da238c95f247b305`  
		Last Modified: Tue, 13 Aug 2024 00:23:48 GMT  
		Size: 29.1 MB (29126232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9989209e08e7247d7cf62d0ace9d0fc1490ff573bc9b88af1e4588c24a757179`  
		Last Modified: Sat, 17 Aug 2024 01:59:43 GMT  
		Size: 145.6 MB (145550052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc523cbd7c08eb01dd422d87d8d0eff7318b80437ed87f488201cea38574ebe`  
		Last Modified: Sat, 17 Aug 2024 01:59:42 GMT  
		Size: 69.0 MB (69023958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9826de9192e05e32a3554e00cfdb5baa2b2303101411f5c564df0279150fe8f`  
		Last Modified: Sat, 17 Aug 2024 01:59:40 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ecc6ea2e89020c6348bc03f62767c819e14ad2cd57d1f3db872dd49bf10f1a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4759102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f4e1b51052aa296a5449b35be9c8f2f6ecac98dbbc2f0206b757162c5c023b`

```dockerfile
```

-	Layers:
	-	`sha256:6e4630842af41e82ff8e03b4e3624475b1b5a2b305aa7dc3ac9f11438bf6546f`  
		Last Modified: Sat, 17 Aug 2024 01:59:40 GMT  
		Size: 4.7 MB (4745164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9acabd5cc9ea28c6f3c776963ad17ad22261158f79e86083d1a8357fd2a4fef9`  
		Last Modified: Sat, 17 Aug 2024 01:59:39 GMT  
		Size: 13.9 KB (13938 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:75c9874015658a8164d41b7c9bf628a82283df515958ce0cb28d3eec0f78d58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240287099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8e741c3663e03151d1fc40e7a39c4364899bfe50887d20b30c80bd24e47687`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:4aa9ddc52f046592777767c91a04b9490d98811bedb8980fca794d55bbad1a0f in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:aa6fbc30c84e14e64571d3d7b547ea801dfca8a7bd74bd930b5ea5de3eb2f442`  
		Last Modified: Tue, 13 Aug 2024 00:42:45 GMT  
		Size: 29.2 MB (29156528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9081243a73eaf94f0cd0715594b5546508ad8c32bcc4ed002229f938f65f959b`  
		Last Modified: Tue, 13 Aug 2024 06:23:44 GMT  
		Size: 142.4 MB (142356408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4614aad3e875558dc4927664edff7fb1ce983582f1ebaf65b0bab9372e3f9dce`  
		Last Modified: Tue, 13 Aug 2024 06:28:03 GMT  
		Size: 68.8 MB (68773519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb763a21a08300050f2d5ab66ade6297406fc528daafe75d73001d92e0690288`  
		Last Modified: Tue, 13 Aug 2024 06:28:01 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.11.4.1474-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:58108f1163a5bbe9052b3871cd4afeb6b3b49ce6bac1859b927085632a7ef0f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4766028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9467ee9e4c09494e9eb739f4bf582f5662b22c7837a4502f62d93e73aa971bb4`

```dockerfile
```

-	Layers:
	-	`sha256:8b7ce6591290d848d08ee7e2a03dde984a985404e52a50dd85b9b506209171cd`  
		Last Modified: Tue, 13 Aug 2024 06:28:01 GMT  
		Size: 4.8 MB (4751549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18dcfeddcc2449bad8357fc36ca3c5faff1ace4aa5c380ea3a4d2775d06d01af`  
		Last Modified: Tue, 13 Aug 2024 06:28:01 GMT  
		Size: 14.5 KB (14479 bytes)  
		MIME: application/vnd.in-toto+json
