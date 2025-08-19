## `clojure:temurin-24-tools-deps`

```console
$ docker pull clojure@sha256:395c063922803317ca7c34dbd1e3e5a3c462ac31e8c41b84ba155c1f54bdbc55
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

### `clojure:temurin-24-tools-deps` - linux; amd64

```console
$ docker pull clojure@sha256:12f4fe482a427fbf27028e2e0e0e4d736203b51789cda5e6c12efcefae8f786e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.5 MB (219513653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5912bb67d5b22e1212d14ba34f65957b6c4f865f33a097c38917dfd373557145`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f014853ae2033c0e173500a9c5027c3ecffe2ffacbd09b789ac2f2dc63ddaa63`  
		Last Modified: Tue, 12 Aug 2025 20:44:32 GMT  
		Size: 48.5 MB (48494511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44f5a94a21e4adc15b35d9fd9e93abefe973ffe7299210fb9185b861532894b`  
		Last Modified: Mon, 18 Aug 2025 16:53:28 GMT  
		Size: 90.0 MB (89975262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3daaa734ea0f8dc4bd599876f8689ec8557a292c31183c70e09cdb01441f07`  
		Last Modified: Mon, 18 Aug 2025 16:53:28 GMT  
		Size: 81.0 MB (81042837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad393ac5bf9c4ab11fe4261739cbdb26bf8f0fae0e25530c135cf5c80a9d037a`  
		Last Modified: Mon, 18 Aug 2025 16:53:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4a687372071e99619fc60550891998f85bd9244f7a5643e569ea86942f5af9`  
		Last Modified: Mon, 18 Aug 2025 16:54:12 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:d58e8f5a9e85b690d57565a6db5b3bcc690bc37a67fc78d221660b5065084f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7336127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fae35630ea8cf410d8565ec7c50ac61eb665cd4b3b5a3170975eb1e0b1ebce58`

```dockerfile
```

-	Layers:
	-	`sha256:d2b70c894a5c3b6410d7c7d3a086b0cc2276d4eb02c68243a643b212968052d3`  
		Last Modified: Mon, 18 Aug 2025 18:42:30 GMT  
		Size: 7.3 MB (7319629 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e524045393346d345f34234e7f0e156b0aa137d568404fda5455cf8a7852166c`  
		Last Modified: Mon, 18 Aug 2025 18:42:31 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:61ca67dacab743326081e4e2884a3a8e170b66db6a9c5d4a5de2738e5ce6a24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.3 MB (218349763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6e24246c1e890752d0672149890222244f3a330b9089231a8f6b20f6b15d88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:35f134665ae4469a16b5b7b841e9efe6b186960e0533131b3603e4816aabeb3a`  
		Last Modified: Tue, 12 Aug 2025 22:08:09 GMT  
		Size: 48.3 MB (48342450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46c4617dcda5b8cbce800f96abfaa1b7d06f73a3bf88c2b640e3d1664a828d8`  
		Last Modified: Mon, 18 Aug 2025 17:20:17 GMT  
		Size: 89.1 MB (89092502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4a8a0beaea4f582c3a889d74657779b68eb050086208bce128aebedcca83e2`  
		Last Modified: Mon, 18 Aug 2025 17:20:14 GMT  
		Size: 80.9 MB (80913771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db21da11eb04288dd7f0bf963704e2c596c000b4aff19cdabbe189c78a54570a`  
		Last Modified: Mon, 18 Aug 2025 17:20:07 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9165ff91f628f1849358ffbee929799e0ed426e803ddec5dea3d78ecef064d`  
		Last Modified: Mon, 18 Aug 2025 17:20:07 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:2eec1ca4b0cf97fc01632b97c2567583f08b6865e10acd94dae1b21bc176f922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de9542d5d8511a391f9e668919237bac17fdc3196c7335b0c49e315349b141b8`

```dockerfile
```

-	Layers:
	-	`sha256:834002cc3457adc2aba618a1d783dc4791c3a47c23e2aaae981b1d41e5d9ac28`  
		Last Modified: Mon, 18 Aug 2025 18:42:37 GMT  
		Size: 7.3 MB (7325413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88d8191a1e98d2e0c36de033cc94d74842c076f4f845e1c0f61c2e72d1c21b4d`  
		Last Modified: Mon, 18 Aug 2025 18:42:38 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps` - linux; ppc64le

```console
$ docker pull clojure@sha256:ba206180403f78c0611ca355b60cc376e1295e8070cee835782306f5dd3542ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **229.1 MB (229126666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4f8db3121f36cf2ca4e74ea3668021d1e04c817a25ac30ccf927ac7aea7756d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:33bc01697f2fcceb00fe53fe1bf433b48dc127c82c1555f61eeddeda9d72ff40`  
		Last Modified: Tue, 12 Aug 2025 23:05:53 GMT  
		Size: 52.3 MB (52338077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51b5f3e32fc0544e0978bc1cbc02cdf94cb71fe8974e5911a37ea4e35f9b9690`  
		Last Modified: Mon, 18 Aug 2025 17:35:54 GMT  
		Size: 89.9 MB (89918259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60aea013107b06ffeeb41a682086fc3958adb27271b09ce251d18651e48e2ea`  
		Last Modified: Mon, 18 Aug 2025 17:35:55 GMT  
		Size: 86.9 MB (86869284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fdc02499f14385bb0494186facd03d21d1c8dcd56fd98fad67ccef7e1d44af`  
		Last Modified: Mon, 18 Aug 2025 17:35:41 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8567e8a16f3725fffce0e658a4cdc7a0ff159f2d2ad9547d5bf1b83914b208`  
		Last Modified: Mon, 18 Aug 2025 17:35:41 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:f958debdf165d98682c0e6425dbc475a88658f307941d76cb0d141a8fd44b1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7342701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00dff966954beca783157980428c0d393ccd3af48dd05466c66b8ac65e886400`

```dockerfile
```

-	Layers:
	-	`sha256:0fb327bd54f5f2dafc22dae2367068e7ad26dc3b43f379716acde1b6a99633b3`  
		Last Modified: Mon, 18 Aug 2025 18:42:44 GMT  
		Size: 7.3 MB (7326143 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b7776c837fcb1a5b3373ca5a58626d5eb9e74e21cf85adcfc1db91d8df010a`  
		Last Modified: Mon, 18 Aug 2025 18:42:45 GMT  
		Size: 16.6 KB (16558 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps` - linux; s390x

```console
$ docker pull clojure@sha256:32ab9a1c7093433ecd5706181e5696ab98af976fd8f5f4e60e7b636390fed975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.2 MB (212226794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4a9e518ee85e4c79ede166efd53b1980584e4d97fb2f5ef5d387c30654aa3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Sat, 16 Aug 2025 23:31:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 16 Aug 2025 23:31:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Aug 2025 23:31:29 GMT
ENV CLOJURE_VERSION=1.12.1.1561
# Sat, 16 Aug 2025 23:31:29 GMT
WORKDIR /tmp
# Sat, 16 Aug 2025 23:31:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b0328626c508af54c3eaf00cfb67e85d5215c6447b15c8ecc70fbe29ca95d64e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 16 Aug 2025 23:31:29 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 16 Aug 2025 23:31:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:635b31fd21bf059b6af0abf57b343066d0218ebb3e0b679927cc1752427a72da`  
		Last Modified: Tue, 12 Aug 2025 20:53:37 GMT  
		Size: 47.1 MB (47149866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9913315ab5e4a25fb7f6b34ab3e3f59fb1ad7999c68ede17552b151576a58ab4`  
		Last Modified: Tue, 19 Aug 2025 18:05:04 GMT  
		Size: 85.2 MB (85226364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcd13e2b87b3583fe09d519081e5540fa72554b6920ffdeb1dabf654450fed6`  
		Last Modified: Tue, 19 Aug 2025 18:05:19 GMT  
		Size: 79.8 MB (79849519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619ef200bca58b22c2d6f6c4fa9844b3457a4691b452f8d7b3c757a7bd6b040b`  
		Last Modified: Mon, 18 Aug 2025 18:09:45 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42caefc0e8ff716574d055a77107b30f480c39a7a18aedc849d2b7ec7577222d`  
		Last Modified: Mon, 18 Aug 2025 18:09:45 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps` - unknown; unknown

```console
$ docker pull clojure@sha256:b3587d8c21ea8fabc268eb1f979b2be3451cff9f935e4fea2699b7b623fe78fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7329994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4959c0a70bb65afdef213dd1ec0a276d0403189f38ad9e9996ac0c8a65508623`

```dockerfile
```

-	Layers:
	-	`sha256:9c2271ea0ed8ede3d0e425c4eb69c7020cca4f63614218c7b9cc3cf017666d50`  
		Last Modified: Mon, 18 Aug 2025 18:42:50 GMT  
		Size: 7.3 MB (7313496 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c5a94dfd393fee363c6a4fd83b895d64d9d408a28882a885cd1339c4a35b69`  
		Last Modified: Mon, 18 Aug 2025 18:42:51 GMT  
		Size: 16.5 KB (16498 bytes)  
		MIME: application/vnd.in-toto+json
