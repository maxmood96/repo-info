## `clojure:tools-deps-1.12.5.1654-bookworm`

```console
$ docker pull clojure@sha256:0b264792a91b4d4664f864ab583f0509e1b5bc83c25c1f01bdbe62a383569c23
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

### `clojure:tools-deps-1.12.5.1654-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:8c0916ab2dcf19e54a442be4597b56cd0db2e6006f84b5b27dbf1f70e0804866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219202909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bc61de8457c24f14cafe7f5a5cd80d63a14b91e36c3502b1fb8038faddd09ce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:20:50 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:20:50 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:20:50 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:20:50 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:20:50 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:21:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:21:07 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:21:07 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:21:07 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:21:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a05b53f5d22894c35a19db0f70b2a3b2521bb5db66425cc339f1e544c572f1c3`  
		Last Modified: Thu, 11 Jun 2026 01:21:30 GMT  
		Size: 92.6 MB (92574589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc998701b978813d19f002b25fbb8b3da0c95b6cfe57423162effef8705359d`  
		Last Modified: Thu, 11 Jun 2026 01:21:29 GMT  
		Size: 78.1 MB (78125237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfa0f4790061f5d3a5c4ae8c165e8e41e6832580bba03018a9fa78b02bae1da`  
		Last Modified: Thu, 11 Jun 2026 01:21:26 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd6b15bc766ca1f7b6977303f87d65d200cc7ce5cfe29eb3770af1e0862b12f`  
		Last Modified: Thu, 11 Jun 2026 01:21:26 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:e27741d16832c7742ae801f28823b69bb5d4a9ab18049b5730b4925a5533f913
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3639c3e75eff699441fac48d7087e9981f16de69c3aca4c3041d6a470868f8`

```dockerfile
```

-	Layers:
	-	`sha256:fee04481c212df0adcb7161ef6870f9782c77be2075e302cd096799cfed5e83d`  
		Last Modified: Thu, 11 Jun 2026 01:21:26 GMT  
		Size: 7.3 MB (7345528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:332c3d8294bbbeb6dbdf88127248cdf67f9a9e5af449e20e099ace68bc32b273`  
		Last Modified: Thu, 11 Jun 2026 01:21:25 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:034ee1035f36f3470c42562ebf697d91c8b3f0b6555663859fef1c0287a20ddd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218061572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09592c019820a40b525c640b751ced3b8ec5a260fa1587b0075961874cbe598d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 01:25:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 01:25:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 01:25:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:25:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 01:25:04 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 01:25:18 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 01:25:18 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 01:25:18 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 01:25:18 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 01:25:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eed48218d91de4725eec7ffd9f0400399a64763874434e49b27834f7efc4fe0c`  
		Last Modified: Thu, 11 Jun 2026 01:25:40 GMT  
		Size: 91.5 MB (91542254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df08be33aee687fe7b1a2ce0082faaf422ec30381357bfcb0be8ef80b9230a0`  
		Last Modified: Thu, 11 Jun 2026 01:25:40 GMT  
		Size: 78.1 MB (78129265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80290229d3aa12ee49045a023c966ea6ef0eff78cf973aebf6eb7b6a7ac54b56`  
		Last Modified: Thu, 11 Jun 2026 01:25:37 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b432b8260a8c25d7dfa4071f5c51e199befd63d8d52419bef368c874a42521`  
		Last Modified: Thu, 11 Jun 2026 01:25:37 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:138309a6380a964e6cb1a69672746a9374e0d4a446fe9e4d6b4109b1cf64dd2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4d2422bef515ad4feb73c4f9c6d82691a2649b312b7420b7f4b73ed2a5cf82`

```dockerfile
```

-	Layers:
	-	`sha256:1e89b86cdab2fadafd169d04e13f923cc3e593c2e02c22662e7b94961590acdd`  
		Last Modified: Thu, 11 Jun 2026 01:25:37 GMT  
		Size: 7.4 MB (7351360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e4ad69d054b8911abbe1564e32dfacabcd94e18ed7e36b7f5ecca7079e194ca`  
		Last Modified: Thu, 11 Jun 2026 01:25:37 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:d2be0a5a88a2982c445332838c8f30fbd83770831156b047aface0c60a416bbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228220366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d7f184b97b079e54545345f8f1fea6e779148c4fc18978777c57e2aec78707f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 09:14:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 09:14:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 09:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 09:14:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 09:15:00 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 09:46:29 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 09:46:29 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 09:46:30 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 09:46:30 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 09:46:30 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5998dd79e03b2035bd6575c617be36964f2fc95c4f35757713e6d58d363b8e79`  
		Last Modified: Thu, 11 Jun 2026 09:17:02 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218c2b9309ce7fed870fcd2a010b9d2131fd5360799f5cbf30e596605cc1a627`  
		Last Modified: Thu, 11 Jun 2026 09:47:06 GMT  
		Size: 84.0 MB (83958650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc408ec8b1522bf5391a21504149beb5fd98253622801b5f5e889432a5c5728`  
		Last Modified: Thu, 11 Jun 2026 09:47:03 GMT  
		Size: 611.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52777e9d6f08c7aea5d353e9430db37fea5ec8884c214c4c641062bfbf326528`  
		Last Modified: Thu, 11 Jun 2026 09:47:03 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d16e1a49b29007ee6f5306e66ae652b155e796814e3a724b2d994cfe6f72254a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:076d6542f89424cfa84afc7f25bb5525f3c2b9950c4438783a033a90abdcecff`

```dockerfile
```

-	Layers:
	-	`sha256:5d755f1083bdbc09f6d36dc9deb010628025993c52a4ae6487cb25e4926b549c`  
		Last Modified: Thu, 11 Jun 2026 09:47:03 GMT  
		Size: 7.3 MB (7334092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:054b5c80af0c9200339691d374a1a75e00ff8ead8ccda6332d443f37b018a0b2`  
		Last Modified: Thu, 11 Jun 2026 09:47:03 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:tools-deps-1.12.5.1654-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:d2e0b764bcd516794845edef96c9b8f2292c70847ce1d44dad9452574b3b651e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212512313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c93d989adafb55de6e64498728fe078c576600b915b33f9978a12a820b151d8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Thu, 11 Jun 2026 03:13:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Jun 2026 03:13:15 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 11 Jun 2026 03:13:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 03:13:15 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 11 Jun 2026 03:13:15 GMT
WORKDIR /tmp
# Thu, 11 Jun 2026 03:14:32 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 11 Jun 2026 03:14:32 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 11 Jun 2026 03:14:32 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 11 Jun 2026 03:14:32 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 11 Jun 2026 03:14:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d5d28a9b892aa865b958e34a0eeffbccb54b6231b8f8f42d3512025b674cad`  
		Last Modified: Thu, 11 Jun 2026 03:13:56 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7e20515be3aa0b952c3fd45514f96a37e4c32fa1d4a2b4f3458165a4f9b7ae`  
		Last Modified: Thu, 11 Jun 2026 03:14:58 GMT  
		Size: 76.9 MB (76929456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f108627d124ccb59ec04aa5a3748b486d94393f99d1361eb2ab9f05414a84e5b`  
		Last Modified: Thu, 11 Jun 2026 03:14:56 GMT  
		Size: 610.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7f9e55a89c8a55d43810ee8dfe90675cb1ec92fb7c35c94ad32924de43504b`  
		Last Modified: Thu, 11 Jun 2026 03:14:56 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:tools-deps-1.12.5.1654-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:3202556704b1e7ef184ca653287bc70143a539f8e7c7c7b7e68f516dd4c72d2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7338381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2bcf3983d8064226ed08af798d9ab1196dfc5ade1ef1f855ed08d4b5ab9daa`

```dockerfile
```

-	Layers:
	-	`sha256:257731cd9317bb7d5450cbb8f3a95432b01a6a22543fe866b29070c5615765c5`  
		Last Modified: Thu, 11 Jun 2026 03:14:56 GMT  
		Size: 7.3 MB (7321409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:354634c0ba960ba3cc5896d07874f071a4d58bbe7104d6b7790e95a13352138f`  
		Last Modified: Thu, 11 Jun 2026 03:14:56 GMT  
		Size: 17.0 KB (16972 bytes)  
		MIME: application/vnd.in-toto+json
