## `clojure:temurin-21-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:81f15c1742f01147e695b261118bededbcb25792e1867a11f7ee42363fd9493c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-21-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:a817bc38ca0e04978332351d50e4f1703195970232060cbcc3d276a69de3e322
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.4 MB (278448950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f97980a85e786f9108784a2f984538994304285c4006d0c3d454ad647410f553`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:46:36 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:36 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:36 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:36 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:48 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:48 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:48 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:d0d98eecfa3b5c942eada879fdb4cf6f79f0b9612ede79322d9d16fc3e984ee0`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 53.8 MB (53768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8357e8e46d40bf5c7226b8608ba0100a7b62db9e6408ad2b43bc30ab74515edf`  
		Last Modified: Thu, 04 Jun 2026 17:47:12 GMT  
		Size: 158.2 MB (158166943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb2b4845f339fa65b83b0e50502230e81e4e6e4c3fe20dd796a717fdd6d11fb`  
		Last Modified: Thu, 04 Jun 2026 17:47:10 GMT  
		Size: 66.5 MB (66512111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e871f8869d28ca783cfcdd05a9ab737858ec90dcbfeecbf3773b6ecba30ab866`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16860f06b395f9a73c81890d8795a95852e4f101ef5d4a59517d8998702272c6`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:deba6a0b2a0112818fe9cca3bd75b2f821a1081ab922d60f57407e2805039d32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7423228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eebd792860af60b8d17954c7fa6fd1d347651e7e5e3343900fcd6bafde73dd1`

```dockerfile
```

-	Layers:
	-	`sha256:9b019746aa63ccfaef9a191c279c26f65a9d26a02f15799d832138e2978a8253`  
		Last Modified: Thu, 04 Jun 2026 17:47:08 GMT  
		Size: 7.4 MB (7407297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34f670c8530cdfc15006fe64356d46f349fdea7ad6f810c69d9cca377682d64`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 15.9 KB (15931 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-21-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f6279c0388509a854a5e3795a7c58b7ee6e8255e89280add5d563c33ceddc16e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275396730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6076ea6d2b610833aa7106d702d7effbb320c2cc1752cb8b0a57bffaf01ae58`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1779062400'
# Thu, 04 Jun 2026 17:46:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 Jun 2026 17:46:33 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Thu, 04 Jun 2026 17:46:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 Jun 2026 17:46:33 GMT
ENV CLOJURE_VERSION=1.12.5.1654
# Thu, 04 Jun 2026 17:46:33 GMT
WORKDIR /tmp
# Thu, 04 Jun 2026 17:46:47 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "28f81b0833c0a072f4370ae0eb1e4c5a4f9f4a34035cd7607ea9f253a8b06da1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Thu, 04 Jun 2026 17:46:47 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Thu, 04 Jun 2026 17:46:47 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Thu, 04 Jun 2026 17:46:47 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 04 Jun 2026 17:46:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:9f08527663b6ddbac974253d3632db7fd8c400d9acb6601fc251de137ec53a8e`  
		Last Modified: Tue, 19 May 2026 22:36:30 GMT  
		Size: 52.3 MB (52256578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22122758a5112415adbf1b41ec50572980981fb51cb7f689340d059c7a8bc164`  
		Last Modified: Thu, 04 Jun 2026 17:47:09 GMT  
		Size: 156.5 MB (156461285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:592ae9e040e3323161e8c8b4c539a2e81da6dbc39294cc16d3956c06a9b796cc`  
		Last Modified: Thu, 04 Jun 2026 17:47:09 GMT  
		Size: 66.7 MB (66677820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d497e608c5bf953ed20a8d7306c9662b16c9a86bacc890558ce65e0a91486a11`  
		Last Modified: Thu, 04 Jun 2026 17:47:06 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faef879fab547b126592113e975d9742ad352113cd646052a16c4dfdaa8c41cf`  
		Last Modified: Thu, 04 Jun 2026 17:47:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-21-tools-deps-bullseye` - unknown; unknown

```console
$ docker pull clojure@sha256:a0e3f20cadc84dbb817bb2b8e1951fbfd3423176d59419e5885f416c0cce4d1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b8c3534e91f1614d0b7705e55992ee5e5632ff6fc7f61dd9782a3ece53a079e`

```dockerfile
```

-	Layers:
	-	`sha256:699dda4754d436e5c840bd5e6fae1a934a818c5175f41f6b0d98b524845b5f66`  
		Last Modified: Thu, 04 Jun 2026 17:47:07 GMT  
		Size: 7.4 MB (7412396 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8580cf38c962e8a895b10f12787395556f35b02e6408c1458a1305b20b1886e`  
		Last Modified: Thu, 04 Jun 2026 17:47:06 GMT  
		Size: 16.1 KB (16050 bytes)  
		MIME: application/vnd.in-toto+json
