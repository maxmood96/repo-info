## `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm`

```console
$ docker pull clojure@sha256:568359c9da60545da02cac8a7e80797640f3aa1add289df751b0feedac4eb4b9
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

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:fc56670578d773bd762f58758e980ff899a7d401e1a703d7701eca7f46995554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.5 MB (275473700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd8476c63a524d4c747f7e56f4a024a150775181ffa31b5e7c8c76bf55cc148`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:18 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:18 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:18 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:33 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:33 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:6a7e0620566c7dfbe5d3c9a7601d116556ec17a021b3e824f8ab09d12b0c25c6`  
		Last Modified: Tue, 24 Feb 2026 18:42:43 GMT  
		Size: 48.5 MB (48488777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a314f31036b2a449609e2d4d3be12fd02532cf52dbe313e0366a6d872e63cfa9`  
		Last Modified: Mon, 09 Mar 2026 20:35:37 GMT  
		Size: 145.8 MB (145806697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d5501f7df55a400984e8dc60a9c529cffc2fcf7bb53079a8c61ce71f1c982f3`  
		Last Modified: Mon, 09 Mar 2026 20:35:23 GMT  
		Size: 81.2 MB (81177579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de448bd87410ce64009f99616467a2ca5e5cad1d846fbdbd17b28e4e5ffe1831`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:0fd4a8a101971d46ae1f7c2bfcb1e766bbbd3f59b521a837711ea19f15b06a75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7412652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75a18edb3d7167055af7fc3191180b377b0d43127f60ffd87a12e28969ce7a9`

```dockerfile
```

-	Layers:
	-	`sha256:e7099f4a1388b6d493277dcfe797c37808f99290849aa8c9cd5527bdbacf0e93`  
		Last Modified: Mon, 09 Mar 2026 20:34:51 GMT  
		Size: 7.4 MB (7398443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c2ad2aa7d74a52d83b6e790fe7e30d5abc6a8cb7cc994e5914b5d8bcab5bd88`  
		Last Modified: Mon, 09 Mar 2026 20:34:50 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f9f53524664cc4a9f65e9e032a3d5d262d167f59c0bb59a8fd69cfd7318f5d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.0 MB (272033597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3d1dcf5a005d6421ba1e38cfc184a4684a1ea70cc4ce52744805f05128ec06b`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:34:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:34:09 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:34:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:34:09 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:34:10 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:34:25 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:34:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:34:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8578011282ae3fef36307f7e3afb2265a96bada1a57648f07bea9cc1a11e7b7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:06 GMT  
		Size: 48.4 MB (48373210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c538eeff47abad0fa2b9657b82d263a4d2ca1fd2e7dd61085ea29c1b0de1f9eb`  
		Last Modified: Mon, 09 Mar 2026 20:34:48 GMT  
		Size: 142.5 MB (142501433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4fe8ab1a4521329ac6eda930769eada9e9d44bf4d178ac63da05500687a430`  
		Last Modified: Mon, 09 Mar 2026 20:34:46 GMT  
		Size: 81.2 MB (81158306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fac3b9b5471bd0fa688bd184d4a8f6ab66b69c8c6d8f6cf9f17ce60ed40866c`  
		Last Modified: Mon, 09 Mar 2026 20:34:43 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:ca0b056f98391b90f7c67ad053fd63e00ea359d60e775258191638f6a9a90a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7419150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c213ac67105fc53364bd64a67d9c71d1b6303b53aebefe8ff809d64cb34e3d3`

```dockerfile
```

-	Layers:
	-	`sha256:1b7dc59c24c73eab69adc34dff789ca2dfa32adb5af7cf17c8d2621ba4e46288`  
		Last Modified: Mon, 09 Mar 2026 20:34:44 GMT  
		Size: 7.4 MB (7404824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:017b35aa93321ff1b5420f90157d4646d8befa75ae99246fa132e01e88c8fa84`  
		Last Modified: Mon, 09 Mar 2026 20:34:43 GMT  
		Size: 14.3 KB (14326 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:c3207a994fe27f0afdf26a7c67574d4614e747354de8838e14137e1dec994881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.3 MB (272335634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e69f308d19f827e4bb5579b4ed0ceb9ab29a8d50475a6d32535b47b6f9178f`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:45:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:45:38 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:45:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:45:38 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:45:39 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:46:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:46:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:46:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:605d3e8e339092bb5c341e87f55fee22f143aaa738eb91d341b5fc6aa27b2b5b`  
		Last Modified: Tue, 24 Feb 2026 18:41:51 GMT  
		Size: 52.3 MB (52336797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403fe91e8aa4cbe7900d756836850a26915a6e3622e92a5a9e11bd5b8b6533b9`  
		Last Modified: Mon, 09 Mar 2026 20:47:05 GMT  
		Size: 133.0 MB (132997814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8395c8c208b01518f450d8b93812d961b3869c25451ced7715ba07c6bf4db7`  
		Last Modified: Mon, 09 Mar 2026 20:47:03 GMT  
		Size: 87.0 MB (87000376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c1fa11ab6de7d28634bd729586d88b88f105d80b9449a05b591cefda17e8847`  
		Last Modified: Mon, 09 Mar 2026 20:47:00 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:01779a4c5ae23ced61b17068e8c784f613ff955c69addcffe0ada9a301c4128b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7417300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6b8683ca881a3658b36b1aeeeb8511c29dcce459c415e9de328322f3a63837c`

```dockerfile
```

-	Layers:
	-	`sha256:8ec6a8bafa1015c19263674aa5c682f257c90250504b57b481152c6e645b044d`  
		Last Modified: Mon, 09 Mar 2026 20:47:00 GMT  
		Size: 7.4 MB (7403044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2857e7030a4791ebe4d06e9d26710b14b5b8c46ce6f6a38918c5626156aa11c6`  
		Last Modified: Mon, 09 Mar 2026 20:47:00 GMT  
		Size: 14.3 KB (14256 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:7f27a02cc04234536aa19d4c6349d0715724a689c8464005bcc3badd4756caf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.7 MB (253699023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7b4bd4764528e5648a16e11247a1f40291a23e98c3ef9c4a48dfa6deebaadf2`
-	Default Command: `["clj"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Mon, 09 Mar 2026 20:32:13 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Mar 2026 20:32:13 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Mon, 09 Mar 2026 20:32:13 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Mar 2026 20:32:13 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Mon, 09 Mar 2026 20:32:13 GMT
WORKDIR /tmp
# Mon, 09 Mar 2026 20:32:30 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Mon, 09 Mar 2026 20:32:31 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:00b1871f38dea81b1982e306480bd9f97cedf7b0cb3342e4bc84925e6082ade8`  
		Last Modified: Tue, 24 Feb 2026 18:41:26 GMT  
		Size: 47.1 MB (47148087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78455097ab053fd4a095369b6037e8270ed42dee2c12d398c3ce66f2d955316`  
		Last Modified: Mon, 09 Mar 2026 20:32:59 GMT  
		Size: 126.6 MB (126562061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:274b70367e0508c833c3d43fd2e1090c13fc6ed4d449a06b77834a13ff680e9c`  
		Last Modified: Mon, 09 Mar 2026 20:33:09 GMT  
		Size: 80.0 MB (79988230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cb70fb717bfa2edb74de6384e733afdc2169bb09b9dcb16b261d5cc1893ed1`  
		Last Modified: Mon, 09 Mar 2026 20:32:56 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-11-tools-deps-1.12.4.1618-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:968d67a6a7e5717b56cabaac16b066e381e749507895ca4940174c3152dbab35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7403975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90a9575e50c28f9f1143c86d8b36e64723c7647d7dd57d940276ca175ea0f9e`

```dockerfile
```

-	Layers:
	-	`sha256:46d3a718b770f046837f53c5a1915388e36b0f635049341757f8669cf31adc93`  
		Last Modified: Mon, 09 Mar 2026 20:33:02 GMT  
		Size: 7.4 MB (7389766 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36e2bbaa200831b12540cc29c9366b511767781d1638610384e179cd779eac87`  
		Last Modified: Mon, 09 Mar 2026 20:32:57 GMT  
		Size: 14.2 KB (14209 bytes)  
		MIME: application/vnd.in-toto+json
