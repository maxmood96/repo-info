## `clojure:temurin-11-tools-deps-trixie-slim`

```console
$ docker pull clojure@sha256:a14a2b4346bc3d8429d665af56de47aa54f7f5cf6601854742210f4d3a9b3130
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d0a57e7076de19201061d64c97c56c0390b574630a5ce752e8c43bded278dd65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.4 MB (247431922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6e9114884b6993338a18ab2b50249115f3c72a9e87213462e59258b7f982d77`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8c7716127147648c1751940b9709b6325f2256290d3201662eca2701cadb2cdf`  
		Last Modified: Mon, 29 Sep 2025 23:35:28 GMT  
		Size: 29.8 MB (29777766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97960a1513520f2eb61e5c85c785e659cbf2f3117c3572f6ac652f36181b6f0f`  
		Last Modified: Thu, 02 Oct 2025 02:07:27 GMT  
		Size: 145.7 MB (145658278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b633bd444d6ef7164e191971aa932e0517cba2bbb7b650b26e0685d19753a6d`  
		Last Modified: Tue, 30 Sep 2025 00:53:18 GMT  
		Size: 72.0 MB (71995235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86f3a1697395203eadb69baddae16245b131f5a4c0f4cc924d2d10e986d877d`  
		Last Modified: Tue, 30 Sep 2025 00:53:13 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:53b1d4225000b2f5c63b76c208be90bcf1dfc046898630a17f63a1dfefbcc26f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5290540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:778d437592fdcafc423c1a36772405e4a1428ec8504573bf36553a9120241f0e`

```dockerfile
```

-	Layers:
	-	`sha256:7c35c185f4f79e27f04f417374a61b110ad457fe1c43528bb3e8e619edd01177`  
		Last Modified: Wed, 01 Oct 2025 15:37:14 GMT  
		Size: 5.3 MB (5276254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7d01d9716740052c7c1338ad9e85d21b684d0f5a33ef375fd54e4ebd18b5dc6`  
		Last Modified: Wed, 01 Oct 2025 15:37:15 GMT  
		Size: 14.3 KB (14286 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:9052a03eac1e8e6eedf4507f9ea278b226b20558142343e222c4658a74a69774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244408536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d16f779ac077b6e073a0cb8c78e14f3057093cd6568079d521a00eeba41713b8`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e363695fcb930d5f18449254c0052117582c3de4263c91575b0a9040c986e412`  
		Last Modified: Mon, 29 Sep 2025 23:35:13 GMT  
		Size: 30.1 MB (30140842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:479635441ec4b26b7c16919caebbb49828500103045e1e70d6f3cc41b34afa8e`  
		Last Modified: Tue, 30 Sep 2025 00:52:11 GMT  
		Size: 142.5 MB (142458743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce497309f2cee10fa5dd005699af01919e8e7d8141beeb53a17b4451e09f73c`  
		Last Modified: Tue, 30 Sep 2025 00:52:38 GMT  
		Size: 71.8 MB (71808307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3094e5e4a2999f7f299c172b508ce86b0b8d14379e70548831a7ab391f598b0b`  
		Last Modified: Tue, 30 Sep 2025 00:52:35 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:7ea3f236a23fe569ed05528a0c63b0b808d25296ab65384d3f7c34d7a30769d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5297045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec9e3f158a71e0f4ad25b0d206cead1e2a191870a3a2fa29718960192c3e1eb`

```dockerfile
```

-	Layers:
	-	`sha256:c4a2ff674b5f797f64b1ed7671504bcac3390ecc255434a70d72330c8fe2292f`  
		Last Modified: Wed, 01 Oct 2025 21:38:06 GMT  
		Size: 5.3 MB (5282641 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3fff6112f5486353b0f259e8433edae8e57520d0b91ff04cbdfad7d9e6259032`  
		Last Modified: Wed, 01 Oct 2025 21:38:06 GMT  
		Size: 14.4 KB (14404 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:0a497a2ccdc20873fbacf31b9f27c27b612b9aaf022e176fad0b8a35bf665544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.8 MB (243847155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90764c47a42af439934f524b7bc063bcaf1ac3f3b43a5fc697f47fba8d2c590c`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8bcecd3ced4047f6a4d35464fc2ee9b45e7fcc10b49690427794f4421b0552ab`  
		Last Modified: Mon, 29 Sep 2025 23:41:19 GMT  
		Size: 33.6 MB (33598454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d92addf3707edf077f9ee7f0964848ee88e86a844932a50e15299603a774dbc`  
		Last Modified: Tue, 30 Sep 2025 13:43:04 GMT  
		Size: 132.9 MB (132852830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c94d0eca6a6537c8134ff5460d0cae9c02f6cebae311e1a6ac491b9abc59df5`  
		Last Modified: Tue, 30 Sep 2025 13:47:15 GMT  
		Size: 77.4 MB (77395227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96d964cd5257cc53ad735eb216894b0fce9db498abdcfccf16cd171a287bff0`  
		Last Modified: Tue, 30 Sep 2025 14:35:56 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:ee159b34e4bea8addf487c9371f1941ee1d00fa8f09c665992569224fb82eff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5294344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f25a1cedf5bb09be8df3b9788f01700cc8e9ce25bc7f8fa94bfb492034b101c`

```dockerfile
```

-	Layers:
	-	`sha256:9f9015079a2309165de7aeda3ea745c99d2fb15dbdd94c61dcd8803e856b1df4`  
		Last Modified: Wed, 01 Oct 2025 21:38:11 GMT  
		Size: 5.3 MB (5280010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbd5f9c9621b94fc74142c3921bc59a60f6cbb3b96ae2bd8668599c250226179`  
		Last Modified: Wed, 01 Oct 2025 21:38:12 GMT  
		Size: 14.3 KB (14334 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:0609ebc173ca61d5e5f565af2b0429a0324bbcad135fbf40e987a447a6c723e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.4 MB (228413691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13236cc723a426d8f597cf23e2fbbccf11e174455e4477f9ae046d178f2c2b31`
-	Default Command: `["clj"]`

```dockerfile
# Fri, 26 Sep 2025 15:53:20 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1759104000'
# Fri, 26 Sep 2025 15:53:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 26 Sep 2025 15:53:20 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 26 Sep 2025 15:53:20 GMT
ENV CLOJURE_VERSION=1.12.3.1577
# Fri, 26 Sep 2025 15:53:20 GMT
WORKDIR /tmp
# Fri, 26 Sep 2025 15:53:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "a55106244ca93ef7b61309e9dca4b248257685870824a8abe2efa706ede8241f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 26 Sep 2025 15:53:20 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:924b0740f35a15fc20142be5c392f6b033c8051daecf16d2db38c22d6d73eb53`  
		Last Modified: Mon, 29 Sep 2025 23:41:29 GMT  
		Size: 29.8 MB (29837230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daf77f610c92a0fd6db1c8adf9bbf547b9bb44a4308f8db16b1543d255dd87f`  
		Last Modified: Tue, 30 Sep 2025 13:16:34 GMT  
		Size: 125.6 MB (125622246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635aa3465bda38d2374947c53b862d7019cb9211f4adc45a71be01cdc2f4c934`  
		Last Modified: Tue, 30 Sep 2025 13:20:59 GMT  
		Size: 73.0 MB (72953571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e8d3ab1f791e4fbfa0421e099a02ce5eefcef27e4fb472490c3ce38679910d`  
		Last Modified: Tue, 30 Sep 2025 13:20:34 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:8792fdf7524590dd2c65a7106a6b18c3935a86d5a722f168fe709801bdf77d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5286467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29012ff832760611c7af10bdd36e536389f475dde4153fc3743e56353ee6484`

```dockerfile
```

-	Layers:
	-	`sha256:591e1a1270295f5a778f41ba8b30d01900900464f334bfc51382a496ec82395e`  
		Last Modified: Wed, 01 Oct 2025 21:38:16 GMT  
		Size: 5.3 MB (5272182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5267bac45f16f28bb820aad4d961dac58d5a193681326fc26e33cc1158b22e8`  
		Last Modified: Wed, 01 Oct 2025 21:38:17 GMT  
		Size: 14.3 KB (14285 bytes)  
		MIME: application/vnd.in-toto+json
