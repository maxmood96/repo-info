## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:38567b5bccd3e4b1b7f89665daa6d1ebab3d156391c02dfc345fe9029437590a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4a74ad8a547e714eb0c58db03ea1c18d91602b62973a512bad35450b1c9f923e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.6 MB (152639929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89efe1c8e6c054e9959ce3f145fde3e358a6b8e41fc9a4cff1d382479e87d4d9`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:34:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:34:57 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:34:57 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:34:57 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:34:57 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:35:10 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:35:10 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:35:10 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ae4ce04d0e1ccb5db08fa441b79635de5590399fae652d10bd3379b231be0ead`  
		Last Modified: Mon, 08 Dec 2025 22:17:22 GMT  
		Size: 28.2 MB (28228418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5e16c670b908dbfeeda3392c1a54950545fe09066bbd92daef5c9a64e0551`  
		Last Modified: Thu, 11 Dec 2025 22:35:42 GMT  
		Size: 54.7 MB (54733369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5bcf5a427b5bc8de156e63a67c50347cd667c7d1e61b8fa5edda027123770d`  
		Last Modified: Thu, 11 Dec 2025 22:35:42 GMT  
		Size: 69.7 MB (69677498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f68ff461bb5ef9f3c7bf9994bb57a160edaeef72f53dfd6787a12f3c4d3078`  
		Last Modified: Thu, 11 Dec 2025 22:35:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:e48975fa11cf763d3ab1e5268330051ca227f474c3907ea5d100a06d58e9b2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5249246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b006ac2d0c5a7f4050ab388e268f5ea971d15b4386617c5786dd3efeb21bc5d`

```dockerfile
```

-	Layers:
	-	`sha256:eea19049143f15cf18a06fad3ab331faf3a6c9d98839cb90cf7d04dc55c6113d`  
		Last Modified: Fri, 12 Dec 2025 01:46:24 GMT  
		Size: 5.2 MB (5234998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5af6bb89f02c639820ce20d281f4e03f0a19204a683f5914239cb8ffbd8a501`  
		Last Modified: Fri, 12 Dec 2025 01:46:25 GMT  
		Size: 14.2 KB (14248 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:845fb5f1d5fa41c9ae99c36d8095918cf4374554fcf510fcb5615445f0cb8aae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.5 MB (151476470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4951a87f7ec8958b9e4a05fab10da01f968a10b280a69f4661a23d65a5b63ba0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1765152000'
# Thu, 11 Dec 2025 22:33:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Dec 2025 22:33:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Dec 2025 22:33:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Dec 2025 22:33:59 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Thu, 11 Dec 2025 22:33:59 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:34:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:34:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:34:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8a4a7306158c2bef7a131de3110e384f4822829cbcce20bc6b4ba32dd82a1d87`  
		Last Modified: Mon, 08 Dec 2025 22:16:51 GMT  
		Size: 28.1 MB (28102229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad526cdd9659e0dea071efce0d96db03f1216b34161cd15a64ebdcdadd4573ed`  
		Last Modified: Thu, 11 Dec 2025 22:34:43 GMT  
		Size: 53.8 MB (53814998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091d942a47b99e9d6916101b4dd1f240ae25774faa544b0bcc594eed4742cc9b`  
		Last Modified: Thu, 11 Dec 2025 22:34:44 GMT  
		Size: 69.6 MB (69558598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac3af129870aa454d09be83249667e30742226ff865a1f5fecf0ff5acf654a0`  
		Last Modified: Thu, 11 Dec 2025 22:34:38 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8e8abdf2e14dfc46c091e6c12ed59b97b6a09eabc303f6414d5cfd76eec8269e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7e4072ec787116946d0a8f8e9718c67e73159bd682f0cab0607019a64500f5`

```dockerfile
```

-	Layers:
	-	`sha256:f8c6ce1d69ef06f88937f4803c1ea42195aa924a516968a8b173f98254d8d419`  
		Last Modified: Fri, 12 Dec 2025 01:46:31 GMT  
		Size: 5.2 MB (5241457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4e8d9d1a961976619d06bb114343ac50b11fd867780d42447086ad6dc05d2be`  
		Last Modified: Fri, 12 Dec 2025 01:46:32 GMT  
		Size: 14.4 KB (14365 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:82cf1307c5c50bdb24aa9ba59b34fcdfb443eed18656e95dfafd2582afc55bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.8 MB (159754403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:370d552b6c469c79da415e4e608df59005a93e58e1a31a2feef0faa5f97b7db0`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1765152000'
# Tue, 09 Dec 2025 16:15:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 09 Dec 2025 16:15:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 09 Dec 2025 16:15:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Dec 2025 16:15:13 GMT
ENV CLOJURE_VERSION=1.12.4.1582
# Tue, 09 Dec 2025 16:15:15 GMT
WORKDIR /tmp
# Thu, 11 Dec 2025 22:43:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "0dc6f211d2a737ce6872feb0aa4d1cbbbe72d02665c684f9ad206b88d2e7f4fb *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Dec 2025 22:43:52 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Dec 2025 22:43:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:85c696326521b18996e4f030a7e27e2c57ad4956710f12ec3011da2c017e09ad`  
		Last Modified: Tue, 09 Dec 2025 09:15:52 GMT  
		Size: 32.1 MB (32068845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f64fb487d3e6808b902444ad63dfe41ea36c5a144cddfa20a3772f42fbf0c63`  
		Last Modified: Tue, 09 Dec 2025 16:16:47 GMT  
		Size: 52.2 MB (52175161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1de750c1418f3cf25868f48058b39043c6fce3acd3d6fdc9a6306d13f04bafa`  
		Last Modified: Thu, 11 Dec 2025 22:44:48 GMT  
		Size: 75.5 MB (75509751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bdb842628be921ffe1df22f8c2c0b3dd72869d0f5f811d5896aefb3cbdc70e`  
		Last Modified: Thu, 11 Dec 2025 22:44:42 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:98159c6c339c425b59fcf167a3f3cd718cc5f7ed1fb9d071036457c839da0945
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5255045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb45a711c417b0fc5649ea571a5d2463aad9331420df9ca64a2305f9ed90b679`

```dockerfile
```

-	Layers:
	-	`sha256:14be6059ad0644fbca72d15bb4edae64a646792894fdff90590c2ab01004fd58`  
		Last Modified: Fri, 12 Dec 2025 01:46:37 GMT  
		Size: 5.2 MB (5240749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22338a12958a79b8d7102e267599c9a97db52cf384e8460d7d591dbcc49bac1`  
		Last Modified: Fri, 12 Dec 2025 01:46:38 GMT  
		Size: 14.3 KB (14296 bytes)  
		MIME: application/vnd.in-toto+json
