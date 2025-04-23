## `clojure:temurin-24-bookworm`

```console
$ docker pull clojure@sha256:97af48519aaa6a2d1fc3dd7685d25498c587dc3b9d77e3632cb0b31f3eae6b77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `clojure:temurin-24-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:23e6eab65b7fb32f866cc437ab5ec0fd751e9ff60188b1ceb01b1d7401052f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.7 MB (221743879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5740300820216488db1003f7df10d3d6e5d8322fb41b3f28f31864a3f169f7bb`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:23b7d26ef1d294256da0d70ce374277b9aab5ca683015073316005cb63d33849`  
		Last Modified: Tue, 08 Apr 2025 00:22:55 GMT  
		Size: 48.5 MB (48490541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c497533bc67ad5307b395824545eebfffb2d91f577a932ce8fb68a16abf94a2`  
		Last Modified: Wed, 23 Apr 2025 17:16:49 GMT  
		Size: 90.0 MB (89951965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192d9598c278046b6b9b8249e0faea8a64b3ae561fcad6e13263c433bb2112b8`  
		Last Modified: Wed, 23 Apr 2025 17:16:49 GMT  
		Size: 83.3 MB (83300327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38683c8296d734a9ec60bc2e46c634f0db85f0d4d33f79cecc837dd2428f7004`  
		Last Modified: Wed, 23 Apr 2025 17:16:47 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4035e7930f1bb3c0f9a0f79288f40769548c3686550e3928526ea5b56766ba4`  
		Last Modified: Wed, 23 Apr 2025 17:16:47 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:98a1be45d5d3ef309d28f1ccb7ad8af7a754202f604e2f2d29c82c36ad0670dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7140303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97b54db4e09392509e52119edba91c607c1b3d533afe293f7ad6b4e7acf883b`

```dockerfile
```

-	Layers:
	-	`sha256:d015e8bc030f30ed966e342d4cc36cf95bc666382f072a5d863a9654537ec951`  
		Last Modified: Wed, 23 Apr 2025 17:16:47 GMT  
		Size: 7.1 MB (7123806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7959cdad7093cadecd0c5a44189a753158f4461d3312501bcbfaeeba9a3b4590`  
		Last Modified: Wed, 23 Apr 2025 17:16:47 GMT  
		Size: 16.5 KB (16497 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-24-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7ead3d95221a79a260cd234528c88b8a4d40c22a78272e3a9de71fc1f4627fe2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.5 MB (220538305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a7d12240bab7ce7439e33f262e1db08da2dcbbf7f0c3c75ec0ce865cc1efce`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 26 Mar 2025 16:17:22 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 26 Mar 2025 16:17:22 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Mar 2025 16:17:22 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Mar 2025 16:17:22 GMT
ENV CLOJURE_VERSION=1.12.0.1530
# Wed, 26 Mar 2025 16:17:22 GMT
WORKDIR /tmp
# Wed, 26 Mar 2025 16:17:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "2a113e3a4f1005e05f4d6a6dee24ca317b0115cdd7e6ca6155a76f5ffa5ba35b *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
COPY entrypoint /usr/local/bin/entrypoint # buildkit
# Wed, 26 Mar 2025 16:17:22 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 26 Mar 2025 16:17:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4532fabbe7464039f3a97caa1f05b2cb98a696be1568a91203fcecc443040bf`  
		Last Modified: Wed, 23 Apr 2025 20:02:52 GMT  
		Size: 89.1 MB (89091255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97a587e934d51a6e1eae51fc23ebe4f53074639ad1f37b36a2000fe464fb13c`  
		Last Modified: Wed, 23 Apr 2025 20:06:52 GMT  
		Size: 83.1 MB (83118536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd64411febf70bd3d30804393d647dd12eb5217a537d8de999b52d72c4dc79e1`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 614.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8b1951c9e874834d0a8bd440d5e77626a7a05a26152061eeba046f900c7b34c`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-24-bookworm` - unknown; unknown

```console
$ docker pull clojure@sha256:2b24cabdb791f90e83447e3da469fdc2aea998fa9194bc4865e3e8d6f46b01bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7146230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff8733ad3c6592712e078ebc1d31242e87a02595bb97760d7e2ff6842bac939`

```dockerfile
```

-	Layers:
	-	`sha256:a9a4ff5b02b8ed07e913b01edb267d46909adf6f03a9e10bcc223eff33d42790`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 7.1 MB (7129590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cec907bf9895192074e987f42303f3da268eb76b1debfd034a80ad536f09d50`  
		Last Modified: Wed, 23 Apr 2025 20:06:50 GMT  
		Size: 16.6 KB (16640 bytes)  
		MIME: application/vnd.in-toto+json
