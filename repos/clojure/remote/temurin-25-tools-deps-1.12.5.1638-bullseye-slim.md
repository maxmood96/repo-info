## `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye-slim`

```console
$ docker pull clojure@sha256:fef7e5ab3efbc53af5aef5c70c6a88120d3d7e7e8289344f6f892cdc33ea8b74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:7bf52c0a972ac85869530932290b9a447b8c92ed70dd24499ec4da749ef250e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (182048767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02edf08e8ff4eed8fd7c0c9311e484a344584bb655e0b1698c64f9122b29eed0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1777939200'
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
# Thu, 14 May 2026 23:36:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:44 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:77e30ef52aeb52d8466baf0f50b54ed2fc0b421f44c49e5bf93682b27110f4d3`  
		Last Modified: Fri, 08 May 2026 18:22:59 GMT  
		Size: 30.3 MB (30257958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03c6ce05e584f6a369af6c1cd202dbbe1262d5db39eaf4fdf9886dd59abf0b9e`  
		Last Modified: Thu, 14 May 2026 23:37:04 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b832ba00379f7dc415a28e9ea4639dae4da3eb9337095a80f3b417349912d279`  
		Last Modified: Thu, 14 May 2026 23:37:04 GMT  
		Size: 59.2 MB (59215198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e3ebe24ed9b4c74b0937c99ce54b6ee43214bb507c01bdb1941ecc2bddcfdc`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b4b566177272caa953f92496fffe32667b653d37c292177f3d5a3b736e5be6f`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:10a40c0f7c8b66e3273f36a06880670572c8ea9705eaacecd075aaa8a64d1411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5305447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:204df34f8ecd4cd399839af75a29da05b78189976203b1650762954fbd7d5506`

```dockerfile
```

-	Layers:
	-	`sha256:d22e620d40d93f6c2be989631321f7305a8d3706822e541a01e4b25e66d4c676`  
		Last Modified: Thu, 14 May 2026 23:37:01 GMT  
		Size: 5.3 MB (5288768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd1c8fce9e196280cdaa7546c511d0d6c332240755f3fd549a85e38528add14`  
		Last Modified: Thu, 14 May 2026 23:37:00 GMT  
		Size: 16.7 KB (16679 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:d9ea578d656b6984c86f3d390a43dc659790c0d14a40ecaa7a8b0b6781cd4e6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.6 MB (179644157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb382144da68d26ca2804bd6bb5d8210d97c0e25d29b6948ec6f7c4fd69322bd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1777939200'
# Thu, 14 May 2026 23:36:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:36:35 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:36:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:36:35 GMT
ENV CLOJURE_VERSION=1.12.5.1638
# Thu, 14 May 2026 23:36:35 GMT
WORKDIR /tmp
# Thu, 14 May 2026 23:36:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bccfca8c437514786f0827a11195b89b833357b2a668091f4321b451b2e36df5 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 14 May 2026 23:36:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 14 May 2026 23:36:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 14 May 2026 23:36:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 14 May 2026 23:36:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ab0f13d792ff9100407906fb422a0b62a8b437abde4c245e03f0366814be9aae`  
		Last Modified: Fri, 08 May 2026 18:25:06 GMT  
		Size: 28.7 MB (28742591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae8fd2d5485b1351fe2b1a465ca0db17bfe3be4f855bb241324580d2e044d77`  
		Last Modified: Thu, 14 May 2026 23:37:09 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80d4bfd9d466dcbae274caa40e66adfde618b30af5f9d2f10a95dca8349739b6`  
		Last Modified: Thu, 14 May 2026 23:37:09 GMT  
		Size: 59.4 MB (59358268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fddd5f6e9992b402534e7d5ba0648b383058f81103bafc9fa489152260cb2a9`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21829f97605ba1be3e43a75cc8146c76b96142f826e582941e1e452059682a4e`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-1.12.5.1638-bullseye-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a617ea4fb49cc76c90d56ab137c2a2b60a9d730495eefe72d12acb1a4be07406
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfaec956977c67021f08d39b90172a5d2828febabc063f69b0e7b9fb55bc2e6f`

```dockerfile
```

-	Layers:
	-	`sha256:0809a5696afd126c70713ca4e3b9b430362e9766c639190148493304958d5f39`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 5.3 MB (5294521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a7c89d51f80a26436791a6476c5fbbeb2409ed098b24b300c46a937752ea0e1`  
		Last Modified: Thu, 14 May 2026 23:37:06 GMT  
		Size: 16.8 KB (16821 bytes)  
		MIME: application/vnd.in-toto+json
