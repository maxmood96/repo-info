## `clojure:temurin-25-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:38ade9467e19d962d19fc92d8af6a63f0d66a649bd02c3f76da2a1ba08246c30
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

### `clojure:temurin-25-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:7143f450605eefc76786469ed79d54007e6a6ab9bed7facbb794acaf3b13e72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **219.2 MB (219202621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5458c8220c97bbb105951733be4656263e66c88a1af73a162c1dcbc449ba71e9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:20:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:19 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01cedcff86f879d042805360ecba268802bec3d8201484ff3ec54f4250a2d3b7`  
		Last Modified: Wed, 10 Jun 2026 23:39:39 GMT  
		Size: 48.5 MB (48502042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dccbe9ce43abc294dd02586243d6ebb9518e3c3f8ca49806ae7b8959f7293e5a`  
		Last Modified: Fri, 19 Jun 2026 02:20:54 GMT  
		Size: 92.6 MB (92574569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18255b3c661e4ad61e00172a81d17a574752a31b81b1a764b33c5d4097aadd0b`  
		Last Modified: Fri, 19 Jun 2026 02:20:54 GMT  
		Size: 78.1 MB (78124970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8c5c44b6de17576662c343989432c828440e0ea898c54e40bc638530896ab05`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2971f341a8f0322d5e4ff303305a6a8da831177b4bc9f6560195646f881057`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:c259e5b017d80aa05f611bad94ded860638e90526905a5fa26521abc26710ffb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7363453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ddf64a92b45bcf8ed24af4d97fe355bda909d8da5bd8fcb0f5a5d5afe8df4b`

```dockerfile
```

-	Layers:
	-	`sha256:aa1887b89b8b5e196ab0068f31781db324ab97cd285a0ea57188b96631974980`  
		Last Modified: Fri, 19 Jun 2026 02:20:52 GMT  
		Size: 7.3 MB (7345528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be48d67c5592282a87a5abecef249830d610f2472a7b11e32ff878b1682bcf9`  
		Last Modified: Fri, 19 Jun 2026 02:20:51 GMT  
		Size: 17.9 KB (17925 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:fe4592e4222cbd79287ad94244dfba8ae547228de699c4ca887fab2df42f4aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **218.1 MB (218061261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a86fa6700b0184b90ba4a6557aa7bb3b1227e52eae1a5291d85debdd1a07d63`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1781049600'
# Fri, 19 Jun 2026 02:20:19 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 19 Jun 2026 02:20:19 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Fri, 19 Jun 2026 02:20:19 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 19 Jun 2026 02:20:19 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Fri, 19 Jun 2026 02:20:19 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:20:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:20:33 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:20:33 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:c847f328095fb083f4a22895b90fe4226efa6458ac57362b64b6e5d99da9e4a3`  
		Last Modified: Wed, 10 Jun 2026 23:39:28 GMT  
		Size: 48.4 MB (48389016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fd2c46073ea530d76d51799915d8bbfe5970eedfda006cdb7ef4b3475e62f5`  
		Last Modified: Fri, 19 Jun 2026 02:20:56 GMT  
		Size: 91.5 MB (91542251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf12474e574358f6598808a8ec06c65c10f5db1fabb11a3a1823f1c8ba36adc6`  
		Last Modified: Fri, 19 Jun 2026 02:20:57 GMT  
		Size: 78.1 MB (78128952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a67bb49ba3415236581393bcad33b4935dee3a58e65e874d4a32eba1a3e69e91`  
		Last Modified: Fri, 19 Jun 2026 02:20:52 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5eef5f9db712b4b11dad87d22959e38ecdecb51cdfda0bec60e910866e93b4`  
		Last Modified: Fri, 19 Jun 2026 02:20:52 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:80d0d46c6e575e474362983e56a81b1a78c547265658241990c857a8f6b2432e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7369475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87eca886aaa503bf906e8925f8b621281e0f5dd2758bee109159150f11881844`

```dockerfile
```

-	Layers:
	-	`sha256:fe3df19ad23faa43e7070b1c355c11cfe6f69ea880961160f70c7cdf5d0da799`  
		Last Modified: Fri, 19 Jun 2026 02:20:52 GMT  
		Size: 7.4 MB (7351360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65db989749098fe471a16524d843dbf0617d17075dbd693e791002cb4b51d934`  
		Last Modified: Fri, 19 Jun 2026 02:20:52 GMT  
		Size: 18.1 KB (18115 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:445e9d668b668a5a044ad114c54e14c26f72714830ae309c4c233a98626e4a17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.2 MB (228220487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f84a45240f3e41cea6c7d5de862a6a0424575eff0aa1c1c5dafca0ebda12b2e0`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:21 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:21 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:21 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:30:22 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:55:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:55:39 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:55:39 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:55:39 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:55:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:88b94a58fac236a778527a3293ccd0ff4d309bff0bf314017ea5af603908fa2e`  
		Last Modified: Thu, 11 Jun 2026 00:21:34 GMT  
		Size: 52.3 MB (52346670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af2d7bc5e0f6f23b949f449ec38352dcc13ff43d0d262dab584e4f344eec386`  
		Last Modified: Tue, 16 Jun 2026 23:35:12 GMT  
		Size: 91.9 MB (91914009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efb0b334fe03d11aca4fe609936d13f88ad2656643ddc16bfea81562bbe9eccd`  
		Last Modified: Fri, 19 Jun 2026 02:56:27 GMT  
		Size: 84.0 MB (83958767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b604c425d54a2507da522d802bb672a141b0243ba67844148088b1e88396ced4`  
		Last Modified: Fri, 19 Jun 2026 02:56:24 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2619c4cd68b73a15b57d109af67ebdd89c474f745aa9ad62370fa4acfdfa4c82`  
		Last Modified: Fri, 19 Jun 2026 02:56:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:4e3ed668f22264c9fe24f9444ba721caa62e0d6275d03e3b0ca330daa2627329
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7352101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f18cb2381e366b4a0c99f4b903a93a2c38e005ceece2ddbfef0d0079c34aa31`

```dockerfile
```

-	Layers:
	-	`sha256:befc66a59ef3c154fd7543e9fd95867509eff66ace09bbcc382f46dcb047d16d`  
		Last Modified: Fri, 19 Jun 2026 02:56:25 GMT  
		Size: 7.3 MB (7334092 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:541b72f39ad956f8e4e5f09cda084d88956c4b1386c5e3ce1cc7fb219d6d008c`  
		Last Modified: Fri, 19 Jun 2026 02:56:24 GMT  
		Size: 18.0 KB (18009 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-25-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:be62d7be813a67016802790eb47a5cf39a02a011071dcf7a0bc79af5105a17d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.5 MB (212511511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d325695b3d671521a1b949d92f0d5ed55efe795dd3b68654f8de64bd6b02ef5b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1781049600'
# Tue, 16 Jun 2026 23:30:16 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 16 Jun 2026 23:30:16 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 16 Jun 2026 23:30:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 16 Jun 2026 23:30:16 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Tue, 16 Jun 2026 23:30:16 GMT
WORKDIR /tmp
# Fri, 19 Jun 2026 02:21:34 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Fri, 19 Jun 2026 02:21:34 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 19 Jun 2026 02:21:34 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b041a55a85cc0e47dd570746852cc1b0fee042f3a03eb250b9f896ac4aa74a3d`  
		Last Modified: Wed, 10 Jun 2026 23:41:01 GMT  
		Size: 47.2 MB (47161500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14907b0f682b8ecfba5edca7e3ae44505f908a9f5163eb33cb4b2d568ad948ea`  
		Last Modified: Tue, 16 Jun 2026 23:32:19 GMT  
		Size: 88.4 MB (88420320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b01e583a20cd57b7b4cf4ea2074f0a86a9fc260f3b323ed6e9e9a5bfe895c5e2`  
		Last Modified: Fri, 19 Jun 2026 02:22:01 GMT  
		Size: 76.9 MB (76928649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9558baa62bf8e7e7657483a91ca54612f960011d65149679431f2a8f7a53422a`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce12932e3926731c5e5c3f79950438a3d5b3d25c94d54c1a31ed1201d3106ac`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-25-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:306c4f3ce0ecb90762cd85ad0fc44647feb6c11743a71f413e55f507c7aec4c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7339332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a044fce2d250ed73a46d44b18b7ee15cf76db0f6c34d3020c1669689bbc2032f`

```dockerfile
```

-	Layers:
	-	`sha256:63a7c760c0abbcab0cc76b95189b49157e7981457bdf0e11102f634bd125e845`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 7.3 MB (7321409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33bf5388d03b1e473c6118806ec0acedbbdca3521c922b7e328ae1b3e36f9048`  
		Last Modified: Fri, 19 Jun 2026 02:22:00 GMT  
		Size: 17.9 KB (17923 bytes)  
		MIME: application/vnd.in-toto+json
