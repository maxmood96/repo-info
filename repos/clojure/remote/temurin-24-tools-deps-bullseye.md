## `clojure:temurin-24-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:9e04b9af6aa487c81829107b3ff15101b74ccb43b10dec29379cf74f761a9da9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:931351b5433137e20619c7e15d772cd8271f5b0dc2b293d09adb514c1c0e4840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.1 MB (213117526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:518358889ffdb9cd06817be939866635bf0465ffb3edbb0f04e26d723879d312`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1751241600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2d765646d883a37610a09973a079fbba4c7596e54d18d0447bdfff142389d1f7`  
		Last Modified: Tue, 01 Jul 2025 01:14:44 GMT  
		Size: 53.8 MB (53754822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334e521940e199784ca84de06ebfa80920166a99da4f768432322e1defeda522`  
		Last Modified: Tue, 01 Jul 2025 14:01:51 GMT  
		Size: 90.0 MB (89952003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc9a03191608d89db5ef2e5d2d68070c396f8b5880db6fe5b91801b4ea3b373`  
		Last Modified: Tue, 01 Jul 2025 14:01:42 GMT  
		Size: 69.4 MB (69409659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb7a1e1b183dece045632031355c36ad47b4671833dea96d89292a880eceb45`  
		Last Modified: Tue, 01 Jul 2025 03:44:48 GMT  
		Size: 613.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ddd87206c9fa34b06a30efaa89c8cf4eed166bf073b0fe13339419b2169a8f`  
		Last Modified: Tue, 01 Jul 2025 03:44:51 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:2437f6656bcfcfd1235bacddba98b697b8c91fc93cd02a46aff50c8d788204ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7362098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55db37c936edd81844db6f242a0ca2ef6b81479f3f119f7237de57420da65803`

```dockerfile
```

-	Layers:
	-	`sha256:8dc7497b5ad8811b035420f956f6a83719a5a21d9df28a5c22862ca3aac2fa2d`  
		Last Modified: Tue, 01 Jul 2025 03:36:53 GMT  
		Size: 7.3 MB (7346284 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc2c261fda265459f8a52e8457c164a021ae72329a3ce646822b989a5ceea4a5`  
		Last Modified: Tue, 01 Jul 2025 03:36:54 GMT  
		Size: 15.8 KB (15814 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8df17be50ff549ff63d0a45bd45067ad5c2609bd1f4d49c2c5c451cd4275ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.9 MB (210882533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd65d94086164b67540bf9fc6f70f1770639d6ed752184d1bcbaad104836cfa`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Sat, 07 Jun 2025 17:38:11 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1749513600'
# Sat, 07 Jun 2025 17:38:11 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 07 Jun 2025 17:38:11 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 07 Jun 2025 17:38:11 GMT
ENV CLOJURE_VERSION=1.12.1.1550
# Sat, 07 Jun 2025 17:38:11 GMT
WORKDIR /tmp
# Sat, 07 Jun 2025 17:38:11 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "aea202cd0573d79fd8b7db1b608762645a8f93006a86bc817ec130bed1d9707d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Sat, 07 Jun 2025 17:38:11 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 07 Jun 2025 17:38:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:01b9f05048bbb73f25cf8fdb677f6390611ed20f4945645387ddce6122b5075e`  
		Last Modified: Tue, 10 Jun 2025 22:49:07 GMT  
		Size: 52.3 MB (52252301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08ee332814ec16846be69923d369819729d6d936efbfe8555656a5ec2ea8482`  
		Last Modified: Wed, 11 Jun 2025 08:44:25 GMT  
		Size: 89.1 MB (89091271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5be0151e228cfcb15193cfb5fe179291c394494c464e9188ec85ac6002b7abb6`  
		Last Modified: Wed, 11 Jun 2025 08:48:25 GMT  
		Size: 69.5 MB (69537921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f6e4b3850acf67ff4b1cccdd7c26ecb2fef2fbe4c8c674a235904c86827ce4`  
		Last Modified: Wed, 11 Jun 2025 08:48:16 GMT  
		Size: 612.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753dd0c69718ebdf2d4952445fce7025dbefb9da469fd085580eacb9053749f4`  
		Last Modified: Wed, 11 Jun 2025 08:48:17 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:7e974863b0fc456601783dbbacc8a726b6c57e5adcd5206773f7113eb8e921f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7367312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c941818b707eeed88543a34756875b01131e38c1cbf9f3a8a9a666113ec0c13c`

```dockerfile
```

-	Layers:
	-	`sha256:22571b2b88f2c2a574bb26ce31ebf3bf020e4e3aace001b5db8463cc1980e752`  
		Last Modified: Wed, 11 Jun 2025 09:41:05 GMT  
		Size: 7.4 MB (7351380 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c23d5daedb4507588bf10b53b725deb62686703aef0490c716ed128160572e7`  
		Last Modified: Wed, 11 Jun 2025 09:41:06 GMT  
		Size: 15.9 KB (15932 bytes)  
		MIME: application/vnd.in-toto+json
