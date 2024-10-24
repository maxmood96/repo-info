## `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim`

```console
$ docker pull clojure@sha256:8c65c80d0f748ce6a423133eb546f26297d728cdbf480e5f0cdcadaa97a8781e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:e10bf150b103738bfc9b3d1eb1afefc33577e99f120a760e7c978a964846f784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196275330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3409e34bc7b33e872656a6a8d6431978e15f0bcb7d1274cb6700431dc4165540`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:0f6f1b93a8fddd20b36a99cc6cfbe4a03bc7be2adb427f7f8e74a2029c54c8bb in / 
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
	-	`sha256:6dce3b49cfe6dc4b4e0198412bb0578215c86dae41303c47438639853bcba562`  
		Last Modified: Thu, 17 Oct 2024 00:24:36 GMT  
		Size: 31.4 MB (31428800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06921a40bdb086f9b6663150f7e6b79963339dc71fe4bed0c995e59e475db78d`  
		Last Modified: Thu, 24 Oct 2024 01:59:09 GMT  
		Size: 103.6 MB (103633964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c77c3abadb836a3271684f28d175977b8b6adf80f3d3f9445993853bd1732c6`  
		Last Modified: Thu, 24 Oct 2024 01:59:08 GMT  
		Size: 61.2 MB (61211921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d0795e43173b3b6bf275bcfb9568393cf24e5a75ba843fbe0d17e6c3a4fac4`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:b7c8f24c393b90dfebc9f287d68f4a4e22d364d3f42f1398a60139c6973f3df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5261616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed9271d98be9a03a03f9504481de37fb5524c041c83f11b688e087a8e1f0a3d`

```dockerfile
```

-	Layers:
	-	`sha256:438660b0abb443626f01126799e852ac8184438db142fd90ec48a86ef7e742c1`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 5.2 MB (5247486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86680dc19d97603a5ef6021e3e756cca896be53ef52ff7e7ab11ca7a8696f7e`  
		Last Modified: Thu, 24 Oct 2024 01:59:07 GMT  
		Size: 14.1 KB (14130 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:e5fbf4c6edcf3af554d924d121476e0ca3f8f14dd7d20e1277ced0db4ade119f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.1 MB (194121044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7554677f6fdafdde64d2d9f16ffebe79fb3b6c8f415b637510cd2cdec3708f6`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 03 Oct 2024 17:49:34 GMT
ADD file:f3f9a52e18a8da911b50ebddcc922d4b5a7aa8caa6eb15fb5c26c696b8fe9610 in / 
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
	-	`sha256:b3c56a24ca3234ee90349473402ac1b368a2fb3c9620242fa70a85d7396d7799`  
		Last Modified: Thu, 17 Oct 2024 01:15:14 GMT  
		Size: 30.1 MB (30075757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd56617999195b0ffb1dc67e741ecec316ed3d649a5eef28e4cd2edf9608af76`  
		Last Modified: Thu, 24 Oct 2024 08:54:34 GMT  
		Size: 102.7 MB (102747708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c435960262df43cf05e7f7a69e91a688f8b5f7a4c94b39453521af8247958018`  
		Last Modified: Thu, 24 Oct 2024 09:00:26 GMT  
		Size: 61.3 MB (61296936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa1ce581441f5c970efa30e4bd66e268aa8cd290b1420d4b6a561acce712db3`  
		Last Modified: Thu, 24 Oct 2024 09:00:25 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-1.12.0.1479-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e1c15858e069959a8f4ed55620bf08fca2988197e2a318df3281129019be6c9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5268164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93768c7959a3e4d0f30cb00eaa7d9490f8fb0d004f1ff7b970b0fa9010f74c9`

```dockerfile
```

-	Layers:
	-	`sha256:f6b30e4f632f24d5af5836df7619c075e3d0a21513a772c802f03e47131b2b5d`  
		Last Modified: Thu, 24 Oct 2024 09:00:25 GMT  
		Size: 5.3 MB (5253922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48099febf26c23e3f0605a85613e9ce1f2ace2d4064f1beef38354f3e1523a1`  
		Last Modified: Thu, 24 Oct 2024 09:00:24 GMT  
		Size: 14.2 KB (14242 bytes)  
		MIME: application/vnd.in-toto+json
