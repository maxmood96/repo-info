## `clojure:temurin-11-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:ddb0aa4a1311778ef52e862338072885f0d7e5abeca6ce36f28fbe4a0c264506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:ab4033285069d7ceb040e117f550bf67a0e5a97541ec8306b361add0eddd0a68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.2 MB (244217104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8fcdea75c4e7dc2eb7900900a58c078af5c8ec496d6eb287fede72c7368929e`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f981318e1bb6063ee0c2cd14bd6e2f0e8ca27aa44c1c06b1dee70337518d114`  
		Last Modified: Sat, 16 Nov 2024 03:51:55 GMT  
		Size: 145.6 MB (145601398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ca6a7822f9c7ee63b3b1454ac7f6e82ba6ad8fc2df01277ec3ff9f7a935b56`  
		Last Modified: Sat, 16 Nov 2024 03:51:54 GMT  
		Size: 69.5 MB (69487066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f87115bc568add14e0dd9967d898f6e35f5b21708ee1b3b63b8bad9023752d1`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:339b62a628c5af64af5c6e6a5c85f33655e207a86af65785a0a48fe13a824eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4955109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4040e1e5af9a46429e550062872e74f19337275e0ad819a9d7321b11cd83c7c6`

```dockerfile
```

-	Layers:
	-	`sha256:5db7c1ab2bf7effa4e57bba5849f3fbd804f353d859a5022177ecca05bbc02f0`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 4.9 MB (4940799 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:135dc67c355ccf86bead5c99072d601b797da69f04a8c84ffef4ed07785f1eb0`  
		Last Modified: Sat, 16 Nov 2024 03:51:51 GMT  
		Size: 14.3 KB (14310 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e80be01a5e3652440d4aa15c20774668bb8683dd7436fcafa92f1d86d3f7bfc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240881938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbcc1c9dc034d48832552ddbca312b22c8ab8f88f39d99992154b0d905405107`
-	Default Command: `["clj"]`

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
CMD ["clj"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52b55715c2acf7d2e0d4e3993e57138bab284227d99b9c0daa802adff868664f`  
		Last Modified: Sat, 16 Nov 2024 05:21:06 GMT  
		Size: 142.4 MB (142389062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc174a48e12620c9d7a8a8d92c1d5bd82dc3faeae827b880bfd384655bd7dbca`  
		Last Modified: Sat, 16 Nov 2024 05:25:30 GMT  
		Size: 69.3 MB (69334874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0e627c65c04ecd2686d151843b7217ad0de5de99007fb3aae829bb632cbeca`  
		Last Modified: Sat, 16 Nov 2024 05:25:28 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:1b4bab5f887b2e5610ab0c91c519b3126f7c4db50b4f59cba77f452b16da713f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4961612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cacf7c23a186e1445ec606e057f29760ef9df791897c4334dd09b8d351ac74a`

```dockerfile
```

-	Layers:
	-	`sha256:6e5c3439a99b59f3b14d597256b38aa2c4061aaee48756b9afa96d5378188834`  
		Last Modified: Sat, 16 Nov 2024 05:25:29 GMT  
		Size: 4.9 MB (4947184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b52174c56215722b29ac841116b9d0d9201f08968713fb69ca2f8d02342d659`  
		Last Modified: Sat, 16 Nov 2024 05:25:28 GMT  
		Size: 14.4 KB (14428 bytes)  
		MIME: application/vnd.in-toto+json
