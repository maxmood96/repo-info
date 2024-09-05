## `clojure:temurin-22-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:83b4cfd6b167c0192da1d4f2f084ebdf66bc942e41b6854370c9eb4937e24141
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:1c11c4796c634df39b4ee32d55468bcc81b8466a1936041bbb7a0210a2f2065e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 MB (254636831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eae396d45b9b96c60574da7035eb2eaf677c9242909e761cd287a2dd008bd4c1`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92d7a7022d30ff92b41b9ef6b1b3dee044c6ea5b95f894dc5e95654427c8541f`  
		Last Modified: Wed, 04 Sep 2024 23:08:14 GMT  
		Size: 156.5 MB (156481578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a6646e8c79fd4304ab12ff8380d97e7b7e1f6a1243d2e164643510d8e33af3f`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 69.0 MB (69027729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7891cc11e55ae8ad78295f6e0491ee913af1cee5bed9813f6944253d1ee887d`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1585b1edb27b455498fb1d2bda5368ab846650136759cd8419089c398253ba93`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:31c66c3944cc3bad2f96656fe7402abae224e213cf3842eae8528a93750f1005
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4760671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15da30635b6f8f208da460a56c146ad10403ca03b9ee97c5f4781d926f08902`

```dockerfile
```

-	Layers:
	-	`sha256:924967ebf25227982e6bfe9617c2bfbe61c4fb1bb7ff257bf183e52cb64e2ab7`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 4.7 MB (4745158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a07811935894e516b304c51e131b74e4e2ddb54aed845e93a24dbcf53968dc`  
		Last Modified: Wed, 04 Sep 2024 23:08:12 GMT  
		Size: 15.5 KB (15513 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-22-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:23d2dc710ae76f8d893279e6ca00393452b2ff4a21a5d70e7289a0b445040088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.4 MB (252434716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dea5b6756c856209d1e654bfaec00e1d322fe045ec1c50afd09253793b55f8d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 07 Aug 2024 18:04:12 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["bash"]
# Wed, 07 Aug 2024 18:04:12 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 07 Aug 2024 18:04:12 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Aug 2024 18:04:12 GMT
ENV CLOJURE_VERSION=1.11.4.1474
# Wed, 07 Aug 2024 18:04:12 GMT
WORKDIR /tmp
# Wed, 07 Aug 2024 18:04:12 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "b23a784c048e4a5b1fc4bcddaea07abcf476621a97d98bbf4f4726c3375d6e98 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 07 Aug 2024 18:04:12 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 07 Aug 2024 18:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d672f973b74af0c2f060cadd4a48c165cd6803d7124a633eb39b6ec8303005eb`  
		Last Modified: Thu, 05 Sep 2024 08:16:42 GMT  
		Size: 154.5 MB (154503671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14237074c2c7ab2826761892738bed484fd358a06c9af9fc227524ce3c6378c0`  
		Last Modified: Thu, 05 Sep 2024 08:20:19 GMT  
		Size: 68.8 MB (68773459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e680d65587be749e38997be7f9b82549d57b31c92415caaffd6133adb45e5bc`  
		Last Modified: Thu, 05 Sep 2024 08:20:17 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041252d9e155998046299110021573d8946167a79c51668c801201a21bf59e96`  
		Last Modified: Thu, 05 Sep 2024 08:20:17 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-22-tools-deps-bookworm-slim` - unknown; unknown

```console
$ docker pull clojure@sha256:09d2e3e3fda2dde537f17ca7c0c00f5eee2ea42970f3899a6f51099eac55bd16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4767597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96644b04f7f3fefd6a5ebcc331fdb152c5f81dd905051bd3de425791349174af`

```dockerfile
```

-	Layers:
	-	`sha256:10031b8fb709f61acae822ebad1af08dc5716062e54401965506f383b6a84658`  
		Last Modified: Thu, 05 Sep 2024 08:20:17 GMT  
		Size: 4.8 MB (4751543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c877ab310eb825c484aa46eba659d6f23ba6a727207b5110a7815397efbd91`  
		Last Modified: Thu, 05 Sep 2024 08:20:17 GMT  
		Size: 16.1 KB (16054 bytes)  
		MIME: application/vnd.in-toto+json
