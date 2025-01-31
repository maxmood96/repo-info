## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:9d0080771f44295d2955cf62f89c9cfab5289d656574b66e75a30db19c951585
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:405bccedebe9a42efa3af7dc5993ee746db38a4a2f29a97d68503a8dd391d0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242282145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05d77a037b276091a304cad53308718986b601b321f73779b01a4d7de55785f7`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872e1faf337987defc773c7544b18f5e44766fab606643c8bff96666fb1b1bb2`  
		Last Modified: Wed, 29 Jan 2025 20:27:32 GMT  
		Size: 144.5 MB (144536746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3fcc97240719162432684c228e144c5a16dfa51ff7c36c3cc5f2092a3ecb05`  
		Last Modified: Wed, 29 Jan 2025 20:27:31 GMT  
		Size: 69.5 MB (69531940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640a18bcdd61202daf7d0ff6faf8dd521352546bbbc381e94ed928857b6802c1`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27ebcc56285d380c441d3868ecb9891120154ddc3aa4d89a14dfd364f662e30`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:51b6e566d9323f2a866ef8854713225b87bfdaa3c8a84d35de30434af0c891df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4928448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24eb78f3f6087d9d791d9018e6308194194e680d9cc6700d6f302275b34d1f42`

```dockerfile
```

-	Layers:
	-	`sha256:05f0662180ddad7931143e641f8c4db712c1c1cb0b1240234cbbe90deb336bc4`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 4.9 MB (4912569 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89d40e6f3c4ec14b1870163c05a1dbd1f5b7d481e81644aa97709cc98834c311`  
		Last Modified: Wed, 29 Jan 2025 20:27:30 GMT  
		Size: 15.9 KB (15879 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5a19e589020e0e4b7da5fd5a2759fa82039cc6af5f72054290b3371b432c5f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240784735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26fd795b559710f0d6a61f796c40c6839db07774478c8f7f20575766e0660b5e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 13 Jan 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
# Wed, 29 Jan 2025 19:11:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 29 Jan 2025 19:11:46 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Jan 2025 19:11:46 GMT
ENV CLOJURE_VERSION=1.12.0.1501
# Wed, 29 Jan 2025 19:11:46 GMT
WORKDIR /tmp
# Wed, 29 Jan 2025 19:11:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "65257085958376a3c89755a6108d67163882c75af709fe8c8918222ca5730aef *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 29 Jan 2025 19:11:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 29 Jan 2025 19:11:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878dbaf01d60d6283547f2fcdacc51188fdfcc4d98d56aaeebf2a89c4dd97862`  
		Last Modified: Thu, 23 Jan 2025 02:45:16 GMT  
		Size: 143.4 MB (143360974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9f034ff3da98ab4e58fbcc2c03af4b4428cc3e9151c51645ad9a0c0101c9d7`  
		Last Modified: Wed, 29 Jan 2025 20:48:57 GMT  
		Size: 69.4 MB (69381689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09cb0c076dc77caf884cd52ad90eb69421f0c45aafb4c9b3c70dc79a49913c36`  
		Last Modified: Wed, 29 Jan 2025 20:48:55 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d673e0e29dd0142e3b4b323a286be2c7a9b99a51bda1ce9e654c9aaa64b765f`  
		Last Modified: Wed, 29 Jan 2025 20:48:55 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:cd6367a9243b8870afa2ddb192118d890ca8cf21d497e4a1e809418f789a4e4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4934326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34a428a4dc024599342fb6a9faec9e3644dcd956da77080e534910ffa77ded22`

```dockerfile
```

-	Layers:
	-	`sha256:f6345290811f1a0e2427cd94ad6d67104bff16b97210338e35c2830d93748827`  
		Last Modified: Wed, 29 Jan 2025 20:48:55 GMT  
		Size: 4.9 MB (4918330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f06e3da2ac13fb37dc1b70bba03941a9e6628325a4580aec0251636f91ca9d0`  
		Last Modified: Wed, 29 Jan 2025 20:48:54 GMT  
		Size: 16.0 KB (15996 bytes)  
		MIME: application/vnd.in-toto+json
