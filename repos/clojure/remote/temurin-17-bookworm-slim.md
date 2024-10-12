## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:5a41656aa695abea5b8dd95d31656b55473ddfec2070041f7b84a3816ed9b19a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c358c0d745ba97a508db662b7b097ffa53538c6769b56291b1ca7c4f9e662a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243776881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd55e75deecfc6196ff0eabeabf42f892f0eeca9d94f0cb641bd7e13700d3364`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:32 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Fri, 27 Sep 2024 04:29:32 GMT
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105c1c2432f659a1a7af9f905ef104c68c6c9b67db8ea317e92b813acc78c3ec`  
		Last Modified: Sat, 12 Oct 2024 00:53:45 GMT  
		Size: 145.2 MB (145166546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e40bd8f141adb3242c272d50524d1f75542075651045504fc4f71d4962a1b6`  
		Last Modified: Sat, 12 Oct 2024 00:53:44 GMT  
		Size: 69.5 MB (69483014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574ffbeb99fc4ed5640d89d378b7573f6d520dc91e2483f3b9ce85dc82c81daf`  
		Last Modified: Sat, 12 Oct 2024 00:53:43 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd40323122687544566d03cf225b09ad22e536d2879a988bab83d648d7bc976`  
		Last Modified: Sat, 12 Oct 2024 00:53:43 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:723f9720d375bbe93d43b55082ad0a68f2ff54713921709e82355009711af55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4909725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e582a86e609bab5e23d6cc01d8c1f1620423bf08498f1eac38d698895c99b8d6`

```dockerfile
```

-	Layers:
	-	`sha256:d441f7f359e855b60d6018e9e309c029346ed5c152e30e6f183fd2f5a95a4474`  
		Last Modified: Sat, 12 Oct 2024 00:53:43 GMT  
		Size: 4.9 MB (4894211 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ef9a1ea9767b86eb3c5ca3703951d9a4870f6e2479f46fb28b19da550e8265c`  
		Last Modified: Sat, 12 Oct 2024 00:53:43 GMT  
		Size: 15.5 KB (15514 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6b750f5783d8f11aea58fb007704e392cf76c825c9b40c55ae08f03520956d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.5 MB (242462330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bdedd1631cd4ecf04d583ef80167bb893556ebf315a8930601198175e952ff9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08ee6331a393471f4851bd4bc2e33934fc8341977da5aca4f907a861ee9a2532`  
		Last Modified: Sat, 12 Oct 2024 01:14:37 GMT  
		Size: 144.0 MB (143959514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6346a57312e1678e4127484f72cc1a96106b186a5b9855f75c274d1640886042`  
		Last Modified: Sat, 12 Oct 2024 01:19:07 GMT  
		Size: 69.3 MB (69345404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6161254a083fae6ced192a4742f82d24f9e0c3b1f3904063b627d0c136638040`  
		Last Modified: Sat, 12 Oct 2024 01:19:05 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b537a5faf1ec727f900b86642b9c3ecbcc0f5d93cedbf75cacfb9ffde7e279e`  
		Last Modified: Sat, 12 Oct 2024 01:19:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-17-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:583862174af3f7f02c2353c878a01022776f99f0fda28c1f2f2a3328ff5543e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4915634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d642fdd7538a887961d6f2e87d849d3f6971815129455c6ce520fd7ebe5cca5`

```dockerfile
```

-	Layers:
	-	`sha256:df947f34b6a02304838924aebc5080c4a675f3096e9016289cc70a17f863cd22`  
		Last Modified: Sat, 12 Oct 2024 01:19:05 GMT  
		Size: 4.9 MB (4899977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50b867d073391ded20bd4c139497b8ad1a773fe060c72f6c808a26d9bea914f2`  
		Last Modified: Sat, 12 Oct 2024 01:19:05 GMT  
		Size: 15.7 KB (15657 bytes)  
		MIME: application/vnd.in-toto+json
