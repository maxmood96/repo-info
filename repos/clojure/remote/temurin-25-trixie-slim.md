## `clojure:temurin-25-trixie-slim`

```console
$ docker pull clojure@sha256:68b7a1d2963142879f784b6dfc4f4c0b8f2b507ebd19151be15452ac92569eb1
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

### `clojure:temurin-25-trixie-slim` - linux; amd64

```console
$ docker pull clojure@sha256:83f1ea850304f147d050fbcfa20330ca5d50fa643d2360c02c5fbf18d2320abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194402988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e957f9fc534fca1813d73e63cc06d7432000f7c6a3f71d0d8ebccf00efeaec`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:01:41 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 20 May 2026 00:01:41 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 20 May 2026 00:01:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:01:41 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:01:41 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:01:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:01:59 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:01:59 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:01:59 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:01:59 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc85245d4e02b9fd58e5ed970d17d53f661c90e04bca983607fb9378943415f`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 92.6 MB (92574564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:873cddf6b50f71ccbd8b31cffcd827444a62a73025a2f259aace424c1d74ac0f`  
		Last Modified: Wed, 20 May 2026 00:02:23 GMT  
		Size: 72.0 MB (72047456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebaa6112a7513f22d111c3352827c4db6d3e674603ad8bc757c8a1608c16923`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16d93b069544f3941cb2aa4ccdd14c62ce01eda1a971310d324d10533963cf8`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:a9a1d4af59fe677f23e79d22bf6a077f5c014a582be8472e38fcc720fcd487b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5244696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ac2f40498278258601deef4ff1513b66105ab021f108aba8a1fa51492e9c22`

```dockerfile
```

-	Layers:
	-	`sha256:c98c55e1a4ad9eaf53b81ae3f0e24753182a85735b1839eb2f4cb9d3b693f853`  
		Last Modified: Wed, 20 May 2026 00:02:20 GMT  
		Size: 5.2 MB (5228049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b42d6e652067663fc073301a71c9b15f30ac6e0008d73874b202b3186cdf160`  
		Last Modified: Wed, 20 May 2026 00:02:19 GMT  
		Size: 16.6 KB (16647 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a2ac7f9a68877a061fb1da01e30a92405940ca6cd922b3327d42789fe055a2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 MB (193557458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ddffe33dbeb40aef7eeed053492860297b6c0c8d931c64b81b41bf77b0037d3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:28:37 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 19 May 2026 23:28:37 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 19 May 2026 23:28:37 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:28:37 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Wed, 20 May 2026 00:08:14 GMT
WORKDIR /tmp
# Wed, 20 May 2026 00:08:31 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 20 May 2026 00:08:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 20 May 2026 00:08:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 20 May 2026 00:08:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 20 May 2026 00:08:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d02a0b02b0a2fee546440b8b26e911492900960a48ada515d3f3d1f5ad32022`  
		Last Modified: Tue, 19 May 2026 23:29:25 GMT  
		Size: 91.5 MB (91542270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632cebfd99c98fb4701c1b9369c61668712375ed97c554a1c71ec25038309eee`  
		Last Modified: Wed, 20 May 2026 00:08:49 GMT  
		Size: 71.9 MB (71872231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a0682bcf72e5946834dc2f3f8fc18899e19b289bf115dcbfd51abf5c6e2a49`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ebc6c883c2855de75563e86aad57d0a13fa99cf43a14abcfc236c1de717f25`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:2a2795e33a185a3eddda0f9ff45c6cbf170a0257e9e166c9711159709d889c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5250620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612029fb610fef27398ee45995145a971448b0bc65ff461b47cbaf5c35018284`

```dockerfile
```

-	Layers:
	-	`sha256:0e1ccbd4270baa5b89a931cb64e0b706090aefe93ee2cb8aeccc07f3164dedbc`  
		Last Modified: Wed, 20 May 2026 00:08:47 GMT  
		Size: 5.2 MB (5233831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e275306d74781b91aa6db6d45827be0b9d4aebab3b6236a133b85339e5449ae2`  
		Last Modified: Wed, 20 May 2026 00:08:46 GMT  
		Size: 16.8 KB (16789 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; ppc64le

```console
$ docker pull clojure@sha256:d1aa6fb91b40d522c33b5ca0d34aae602c1c4328e9863e842510b982ca231b9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.0 MB (202969355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2726c90117f25ec0e30aaccad9d3183550fe7d9576cbe415b59e4987c6e40e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 02:43:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 09 May 2026 02:43:32 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 09 May 2026 02:43:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 09 May 2026 02:43:32 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Sat, 09 May 2026 02:43:32 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:34:42 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:34:42 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:34:43 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:34:43 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:34:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac28bbda9cf605f0d239dc381ad9eec484e7e0bec93b2a70b5e743abff1b6d9`  
		Last Modified: Sat, 09 May 2026 02:44:39 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9db61fcd9ea473ede1ac67f1ddb14e52efd89351703890aee8ab9bc44a8233`  
		Last Modified: Fri, 15 May 2026 20:35:17 GMT  
		Size: 77.5 MB (77456213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f962c6f2cb0882206a258463446a13cb0a20734e16441bf0df54d85f65b402`  
		Last Modified: Fri, 15 May 2026 20:35:15 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10206182cc9417b515209764a4421ff8da7c6972f97388f14b28cb2bbe2a95f`  
		Last Modified: Fri, 15 May 2026 20:35:15 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:804e0a2b072d0726e4e576ec477b9e813d4a171c2fcbca28432799c8b4fd6c08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad860a06bf0220b12578ef6f0d3b4ddbab92057ad842d85cfe65b0606bc795f`

```dockerfile
```

-	Layers:
	-	`sha256:dec1bcf0a3e0bb4f99d1ce16d4168ebf763cfe25001b7fa4104116256e6ed5d9`  
		Last Modified: Fri, 15 May 2026 20:35:15 GMT  
		Size: 5.2 MB (5215630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85012c6062c5a0af504b6f918cdae263658dd89445a11912b6906093bf87dedf`  
		Last Modified: Fri, 15 May 2026 20:35:15 GMT  
		Size: 15.8 KB (15754 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-trixie-slim` - linux; s390x

```console
$ docker pull clojure@sha256:cbf63c4cfa81967970758583b0c4783607cb65410bb7a5d6848f9dfbd246ac4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191276789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bc420a753a59455ed5b52f47bd28e182b7637eeb2395ff8ca0b0b512402960`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 23:38:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 14 May 2026 23:38:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 14 May 2026 23:38:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 May 2026 23:38:16 GMT
ENV CLOJURE_VERSION=1.12.5.1645
# Thu, 14 May 2026 23:38:16 GMT
WORKDIR /tmp
# Fri, 15 May 2026 20:37:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3d6e8428fd4c7f76de9f87f77b2347f293109f4e88fb20c154b3fa34a7f687dd *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 15 May 2026 20:37:05 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 15 May 2026 20:37:06 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 15 May 2026 20:37:06 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 15 May 2026 20:37:06 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6952bb1d663535da0dd5c38e39c53fd423c23c012766a00ed8340a9bae4ab0a1`  
		Last Modified: Thu, 14 May 2026 23:38:59 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6987d6a096ae06ee3041901bfe2c3e5471e969cf5f7c64501fb7372498efc3b8`  
		Last Modified: Fri, 15 May 2026 20:38:05 GMT  
		Size: 73.0 MB (73015078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57936e9c840c0418cc1d1337728e3f9db9cdd025ba3fc44b1708ae61eccf96d6`  
		Last Modified: Fri, 15 May 2026 20:38:02 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5ec6ec533102f44a523b01a93a57735b8670d7b60ca27bdd0efa304db24800`  
		Last Modified: Fri, 15 May 2026 20:38:02 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-trixie-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:c598edef25391b0fb0476463b4fbbb72722f412ead1f000a20293d371b671171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f47d15c7c95284421bee0662c1a19d7806ca82c913585be8b78a8b8cb82f11`

```dockerfile
```

-	Layers:
	-	`sha256:1ed6cee054ef786239ecebf31b4c9807d78d2a20d2fd75ad43677915b4fab6c4`  
		Last Modified: Fri, 15 May 2026 20:38:03 GMT  
		Size: 5.2 MB (5208421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d13912b36c675772dd469a141a23c0a60fbba1759853d0114e9488efee878883`  
		Last Modified: Fri, 15 May 2026 20:38:02 GMT  
		Size: 15.7 KB (15694 bytes)  
		MIME: application/vnd.in-toto+json
