## `clojure:temurin-21-bullseye`

```console
$ docker pull clojure@sha256:874e954f81c7bdff0d9b49a8d6b0f15a0442c94c75de39274a296d20bdd0e2a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9cca5cb8954047494096d7520e7df09ccf6db6f1b1a746d5930f37ed1aa068b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282995455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed5ff5a8a36a88f92f47ac20d2dfc75575028d52655245cd49d7c852a337fc3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eddb54a5c14756d3e7cfce88fe77614837abe76613ae35517baf5f354304118`  
		Last Modified: Sat, 12 Oct 2024 00:54:01 GMT  
		Size: 158.6 MB (158579253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:185271533e878119fa7684f1864f5d6dd60577b4bbb5d67e67b820c6385df58c`  
		Last Modified: Sat, 12 Oct 2024 00:54:00 GMT  
		Size: 69.3 MB (69333766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6638ce67086a41847d9f445170fcf16246f0fa3fefb5cd3cd59bc2be89cefb81`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96fe67b117675c02c6b8e5caec30e1bc527b31e5f5834626f4b9114047ea688d`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:c994966bcc31e12807d0e151bbfb8bcd6367bea72afd070f259effa574ae68cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7209934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aea4548a7aa048943de94ffbf304d663c15c7b40830c30ebe79a3cac2501e7c6`

```dockerfile
```

-	Layers:
	-	`sha256:873315cce8e89e6cf4684319ef6ed0243a923d7196962a336ed975cceecc269a`  
		Last Modified: Sat, 12 Oct 2024 00:53:59 GMT  
		Size: 7.2 MB (7193780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c0280b226cabd055dfd73b5842ba90259aff59ad7b0f3e1a14a049eea09d37`  
		Last Modified: Sat, 12 Oct 2024 00:53:58 GMT  
		Size: 16.2 KB (16154 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b0b3261e9f39b65952bbf30092e31e6605f97b8c3d0ccb297207e249fb12ec20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.9 MB (279948090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e302a018ffc7ba1395f31516f83829fb1c720ea35900954f635b9ce521af960`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d63d336c3ffd8ca47d040968252435d0359996fc6053a1e58800d5fd2b5675`  
		Last Modified: Sat, 12 Oct 2024 01:23:53 GMT  
		Size: 156.7 MB (156746254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5139e28389b2bb625b715fa416e5591f7e0b2333c6c2008face5e2b6d9860598`  
		Last Modified: Sat, 12 Oct 2024 01:29:02 GMT  
		Size: 69.5 MB (69466929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecec5c43466d5a0f246feecb752c8529782fd551297c4626c9ef65141766d5a`  
		Last Modified: Sat, 12 Oct 2024 01:29:00 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3431893b8f1e6736cd79acee1794591d9f319b9ced4dc1adc99fc95923f4b38`  
		Last Modified: Sat, 12 Oct 2024 01:29:00 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:e48c6db90eaaf4da7340d2fb0c4fdaf2d48d9eaf646cf8781c3286b127349678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7215191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9b93d95b25838016efa3b2bfd37b8b9dd147269957230a500bf6a02b693c2ef`

```dockerfile
```

-	Layers:
	-	`sha256:ec2c5cfc39eef4038f50231822208e9785f15a45c29c3ede975102bc28bb9491`  
		Last Modified: Sat, 12 Oct 2024 01:29:01 GMT  
		Size: 7.2 MB (7198907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3badad120aa14c39e83edd60e56edbf187b56cefd9dd9e6c4d0585f3eb92be0`  
		Last Modified: Sat, 12 Oct 2024 01:29:00 GMT  
		Size: 16.3 KB (16284 bytes)  
		MIME: application/vnd.in-toto+json
