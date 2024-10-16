## `clojure:temurin-23-bullseye-slim`

```console
$ docker pull clojure@sha256:33368efce51403f6572623610722f4048844184f198bce662204f90bd67eeb31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-23-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4bd040ce192b4cfe284cff1f1ca14ef0266a82a36ca6ca7fc033da2e7de29158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.6 MB (255637452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c92c0eca788520b3c8eea99df2d13ff3238bc35939d4832a591cf1de91452`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:55 GMT
ADD file:270cda9833ffe6dfbe916662a9204a205f41c1fd440b66ec822ac00de86a5f5e in / 
# Fri, 27 Sep 2024 04:29:55 GMT
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
	-	`sha256:fa0650a893c25858ebb09921bc9b7824594e23405374a6adbcd3b4e27e28e3cf`  
		Last Modified: Fri, 27 Sep 2024 04:33:50 GMT  
		Size: 31.4 MB (31428599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c155e61c0f1e353b927bd67b03350abd90cc1f5782af94924d9a26d2201c8a1a`  
		Last Modified: Wed, 16 Oct 2024 16:14:29 GMT  
		Size: 165.3 MB (165267628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34de6e801dd1fca9d941a998d03b06108f450148e25f941c61810632fa443ab`  
		Last Modified: Wed, 16 Oct 2024 16:14:27 GMT  
		Size: 58.9 MB (58940179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1232de9c900f564407c4f5c23309c693b83d65ca02fcf1ef184989e39cfe1d1`  
		Last Modified: Wed, 16 Oct 2024 16:14:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e048c6dd87e3b1012f4335ae6152f35fcb06f32aefe91170840e0f2529b4db`  
		Last Modified: Wed, 16 Oct 2024 16:14:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:54e28ab583e88cd8f158826a656b1eb65f73c1f7e4a9c3cd1c9744f8b60842a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5120029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675853286f921399c378e0d0d7f5833d52cf290a8cfa33179bc227e3efc7eae0`

```dockerfile
```

-	Layers:
	-	`sha256:abd84c86b2d181250e8d487bb12026fc2f3c63cc081aab6c13fde93b8c3be158`  
		Last Modified: Wed, 16 Oct 2024 16:14:27 GMT  
		Size: 5.1 MB (5104478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46d7856a43dfe6f774e1f1fe12a56e9f4aa9165746cfda94fe6713733779384a`  
		Last Modified: Wed, 16 Oct 2024 16:14:26 GMT  
		Size: 15.6 KB (15551 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-23-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9a84a9693c5726e9ee20f84e36a3cfd6e78ee619f9ee312ec0152e7836efe0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252402351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1214da1f33991d66650aedf844e890b81a607528aeb1655d43fff93054edc96`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:32 GMT
ADD file:a981209c874e612fdb9f74c3315954986cfdc61cf22ab48477f2e96b3e7aeedf in / 
# Fri, 27 Sep 2024 04:38:32 GMT
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
	-	`sha256:2245c7c084558dcf55e2bad9579c63dfdbd831cdbed2e063a1c25322cb793bed`  
		Last Modified: Fri, 27 Sep 2024 04:41:27 GMT  
		Size: 30.1 MB (30075158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e41c8aee46923b85d416154b4ad4adf86f1fe9e3faddd049e229c3bc3e0ba90`  
		Last Modified: Sat, 12 Oct 2024 01:35:12 GMT  
		Size: 163.3 MB (163252810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d442cf097cfd9a4571e3bf2ebdfe9006efcd005d2ce9601e9b0d6be49d61b9`  
		Last Modified: Sat, 12 Oct 2024 01:39:20 GMT  
		Size: 59.1 MB (59073340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163bab70ecc92a264a639b0109408a07b29796cde0695660d28be8d20498f1e2`  
		Last Modified: Sat, 12 Oct 2024 01:39:19 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8a9a809495a9a3680d62546920075b2fd635f822e7d996f91b0b785bad748`  
		Last Modified: Sat, 12 Oct 2024 01:39:19 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-23-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:6f31b815358ce2090c8fb7c08348ce78ddd2ba1df48c01b950aca9513a0f6594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5125250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de893aa254921ad874d01757c609a0896e7804d04046c4c004f75d69eb8de7c`

```dockerfile
```

-	Layers:
	-	`sha256:22a4c4a985df5fcbd54ca0b1f3d8a208a929473b93e3c080c666d6d566ca349c`  
		Last Modified: Wed, 16 Oct 2024 02:43:16 GMT  
		Size: 5.1 MB (5109593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c232b26c74dccfec0a9370b4922f647d66ae120f5a6076fb61199e42cc01a324`  
		Last Modified: Wed, 16 Oct 2024 02:43:16 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json
