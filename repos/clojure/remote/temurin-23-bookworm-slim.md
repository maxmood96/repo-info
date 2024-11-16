## `clojure:temurin-23-bookworm-slim`

```console
$ docker pull clojure@sha256:93d0e0960b0285db9dbdf86177cb6e571afa8abec10ef3848f970ecc2f4cd4a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c3611f8e4cfec184b4e5bf809c88847065547dc09a8324e3a4c7d126e1a9cd07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263911391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3293fb89a0b2b9af7062cf35596ef3eae1fb17795290c4e88ca24d200ec282da`
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
	-	`sha256:0dc58329d931d82e09f83e2f9a4bfd305408f1f761ebfe2f1b0dadc050e0d3ba`  
		Last Modified: Sat, 16 Nov 2024 03:51:52 GMT  
		Size: 165.3 MB (165295087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881974135cd9230da9f4207e96f3e0e0821a7a4c6e1d65d84ba9ded63b900c4d`  
		Last Modified: Sat, 16 Nov 2024 03:51:53 GMT  
		Size: 69.5 MB (69487269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8500218364e162823f74446d3166916e246f94e278f9105ffee2b512a6be4d`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29120b1a5d75dd00bf6ba6f35b0a5df81f679a6861c278ed1880b470430ae6`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a8785937f20bcffbd632d405e3b37fed4a7187fa411ee5e9b20d71f5a64bc4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4941519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020524f39898172554a521e15f1e0c8d73bd8c194c405bcb9e9239eaf3474f35`

```dockerfile
```

-	Layers:
	-	`sha256:9ce082e0148ddfd7a012339bddad5ebe8b5afcc6f08be635e5d353f2c276a81e`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 4.9 MB (4925641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9f58b843e22350b8844b95cca5a03dfb1219ef31ff7000ccb424f2b46a3d124`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
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
