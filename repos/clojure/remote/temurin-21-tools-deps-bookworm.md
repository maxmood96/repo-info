## `clojure:temurin-21-tools-deps-bookworm`

```console
$ docker pull clojure@sha256:95633509b6f42099d32421a8630b65010c283b654409ba80bc4ba35404d673c2
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

### `clojure:temurin-21-tools-deps-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:ca3c82998fb533484489909ce156901aed93f72cf006a9b371fcc19d5ecb249a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **284.8 MB (284795326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c0f3922660de005318f32dbae5def5a9dd82ecef1b3622bb772a4c8f061f90`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:19:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:19:29 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:19:29 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:19:29 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:19:29 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:19:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:19:44 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:19:44 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:19:44 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:19:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:425befdf76e52426879d2abe42093a00dca59a893e7b4fa2a7679b0180b71d4b`  
		Last Modified: Wed, 24 Jun 2026 00:27:40 GMT  
		Size: 48.5 MB (48502210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678d4591ddcc28de0689396e5190b8728ee8f8b9951d3120627b4ce7a5d2836c`  
		Last Modified: Wed, 24 Jun 2026 02:20:08 GMT  
		Size: 158.2 MB (158166926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304180bfb0f23cca96c83f33962abae0aca3b4eb87207e3658d6a2c74dfb8220`  
		Last Modified: Wed, 24 Jun 2026 02:20:07 GMT  
		Size: 78.1 MB (78125149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b120762c49493788fa7c81155a70978e8af3abae7f3ce717067c0d3f29121a3f`  
		Last Modified: Wed, 24 Jun 2026 02:20:03 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72763c93e07505462fb33588493414ec7a4a43e15abb115331c9f0ad2c53349c`  
		Last Modified: Wed, 24 Jun 2026 02:20:03 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:21902bfc1d9a9b95f28c52b1be2e79641c22fe8424635a5cefcb90bd68a2f215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7395285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f00acf09f8be5a96813e7f40853d228533a22c77b3be4ca5b7d67609b50cda`

```dockerfile
```

-	Layers:
	-	`sha256:b02a9bd03b83c560a8d952df7d6f847448b5bc875184349afa2c5eb2b8c00071`  
		Last Modified: Wed, 24 Jun 2026 02:20:04 GMT  
		Size: 7.4 MB (7378670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b7c5b6488e4a4cbb9954ba3fd844b7b733a4f631b0ecb0384a6bbf0c8fe72a2`  
		Last Modified: Wed, 24 Jun 2026 02:20:03 GMT  
		Size: 16.6 KB (16615 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:218469e3a10d0934fce88fee63ddd2dd902b31c0ab1be200849683155517918b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.0 MB (282981351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea66e7c806f2db92f5cd293a1ec776f51791d550ebb121f88a71608c6638680f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:25:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 02:25:59 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 02:25:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:25:59 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 02:25:59 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 02:26:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 02:26:14 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 02:26:14 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:0fb1189398e2e4b474d43aac6502510d0da0318e70137a377c21087f198814db`  
		Last Modified: Wed, 24 Jun 2026 00:27:19 GMT  
		Size: 48.4 MB (48389201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18aefff1f7a59c8b8b4356d25fee763811f17dc1e1a63105c46349ca6cc016`  
		Last Modified: Wed, 24 Jun 2026 02:26:36 GMT  
		Size: 156.5 MB (156461287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e386f1ee2b7813fd916ec026f0cfe881b68d15329efc35304841a2305b61695e`  
		Last Modified: Wed, 24 Jun 2026 02:26:37 GMT  
		Size: 78.1 MB (78129822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7bc8dddd144e8025c47a187391808bf011c923052f39c3b18d10e3225b02c2e`  
		Last Modified: Wed, 24 Jun 2026 02:26:33 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257d1f24172194e7259c15a6cbd5e200774f9bfae56b60bbc7bcdaae052c53ca`  
		Last Modified: Wed, 24 Jun 2026 02:26:33 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:8a74fe8eb1b0942693601b44c6cead004d397f5eb5891ea7900f571c22f53308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7401215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65af1b82b847fc2c380c7862ee2329f66c88af4d1a66f66f9261dd76b08a405b`

```dockerfile
```

-	Layers:
	-	`sha256:03a13f312863af3a9c8a04f2f82225b086004231647c29afe56405ec97b4c93b`  
		Last Modified: Wed, 24 Jun 2026 02:26:34 GMT  
		Size: 7.4 MB (7384457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b512e4c6eb1c559896e13475a3be522564f0cea11e7acbdbec16b1f5480c1b1`  
		Last Modified: Wed, 24 Jun 2026 02:26:33 GMT  
		Size: 16.8 KB (16758 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; ppc64le

```console
$ docker pull clojure@sha256:14d7da85c6568d14a415fea4c5b6e266aa5da0774f834cc7b186f8c514b35831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.6 MB (294649947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b052cc24e60ecc31876628015297ce6104942d6410aabbd88a2dc37a77ece4cb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 08:11:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 08:11:43 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 08:11:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 08:11:43 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 08:11:43 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 08:19:45 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 08:19:45 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 08:19:46 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 08:19:46 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 08:19:46 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:55b0e891f4e8dc14bf4bc7e853254fcf1f3ba5a8e8e3c07c21e7dd5bd6d87882`  
		Last Modified: Wed, 24 Jun 2026 00:27:34 GMT  
		Size: 52.3 MB (52346847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b243922f32777162d6293cd958624c070d9e6bf6ae5dbe45719e167e86cde0`  
		Last Modified: Wed, 24 Jun 2026 08:14:59 GMT  
		Size: 158.3 MB (158343212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d18ab35f2003145408982f86ab8815d0ba639cff5802cc8a8ff0f36808f363`  
		Last Modified: Wed, 24 Jun 2026 08:20:21 GMT  
		Size: 84.0 MB (83958848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e9a3771811b7f191c95b758e9c23f64a7a60601c5f8c3cf565086ee0784f29`  
		Last Modified: Wed, 24 Jun 2026 08:20:18 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c456792bc2bd7628718219875b217ae1e35c25fcedbb59942eea2d9899e299`  
		Last Modified: Wed, 24 Jun 2026 08:20:18 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:d49f281ff3a371e1494d6f8be1c0edf6d864e6308a9eace832ffc1efb05cb2d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7400574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f73b92d377df53e6b4ce43ee73766917161887722ac3e16d6974dcc1ce1eaeee`

```dockerfile
```

-	Layers:
	-	`sha256:3cbb7380f9d254b81a1129389deaabf724e9575edd45cbcbaf64955ff6cfd2d1`  
		Last Modified: Wed, 24 Jun 2026 08:20:19 GMT  
		Size: 7.4 MB (7383898 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:734afc64694bc4af94b0d58dfe409c6380615b9b5e4b9746d3901a53b808bcf1`  
		Last Modified: Wed, 24 Jun 2026 08:20:18 GMT  
		Size: 16.7 KB (16676 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bookworm` - linux; s390x

```console
$ docker pull clojure@sha256:8e7ab626671c73020c1f7a7e2b3bc47055d562cfe8dcfe21303d2d3d7033228c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.5 MB (271480275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dc8dd37ac09210475f1d97c524a657b14efd81c5084bf5fa1748ba1e30c7170`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 04:14:04 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jun 2026 04:14:04 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 24 Jun 2026 04:14:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 04:14:04 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Wed, 24 Jun 2026 04:14:04 GMT
WORKDIR /tmp
# Wed, 24 Jun 2026 04:16:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 24 Jun 2026 04:16:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 24 Jun 2026 04:16:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 24 Jun 2026 04:16:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 24 Jun 2026 04:16:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bdd2e9d83d68023204331dd445067114dbd3500d2d496368624fa7ef81743d4a`  
		Last Modified: Wed, 24 Jun 2026 00:27:09 GMT  
		Size: 47.2 MB (47161675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee288d67ec7e9d3f16346468657d9b92cb88d075c672782c475a601fcdc7be0`  
		Last Modified: Wed, 24 Jun 2026 04:15:41 GMT  
		Size: 147.4 MB (147388408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8039e9d0c3e350e804673f36f0cd1f1ef2e00ffdc42c3686767a2f982c92f5d`  
		Last Modified: Wed, 24 Jun 2026 04:16:38 GMT  
		Size: 76.9 MB (76929148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea516fc652a34d7944e268009941315adea1cd8d74780e5004e40a2e6de79dd`  
		Last Modified: Wed, 24 Jun 2026 04:16:36 GMT  
		Size: 615.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f81d69d6a45bd0b1910202edeb2079fd0f4496cf891ea548a4508977ef430ddf`  
		Last Modified: Wed, 24 Jun 2026 04:16:37 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:f6c95e02c7c1476bf8c24f1416689c6fa0bc6b19cc2bc6257d2c1c908d6f3526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7386605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a2066e15eb7ea01ad2a92b908dc65942d871c7253adaa34e41ed7ec316ad77d`

```dockerfile
```

-	Layers:
	-	`sha256:aa219d5caa2b5680aa7fca146b39792ff93e5e22cd6006499e67eddab9832c24`  
		Last Modified: Wed, 24 Jun 2026 04:16:37 GMT  
		Size: 7.4 MB (7369989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4ec843983ae958803b73d8cae4dfbee34b79541a96700a429df14ca8dd464978`  
		Last Modified: Wed, 24 Jun 2026 04:16:37 GMT  
		Size: 16.6 KB (16616 bytes)  
		MIME: application/vnd.in-toto+json
