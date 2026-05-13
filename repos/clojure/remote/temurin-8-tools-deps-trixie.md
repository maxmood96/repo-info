## `clojure:temurin-8-tools-deps-trixie`

```console
$ docker pull clojure@sha256:d8a0b81d18aa2bb2a5e85ee8905c8e4c69ac326894dc9eaf876e7e387bee2eea
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `clojure:temurin-8-tools-deps-trixie` - linux; amd64

```console
$ docker pull clojure@sha256:ad133fa4db252e09f1bb8e163ebc1b9902e0faa468cc4338f4255605ba1e9c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.1 MB (190072616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1533fa8276fd62bf2df37b12747e719194b7db18ed5230566ca8684fc38fa300`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:46:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:46:07 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:46:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:46:07 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:46:07 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:24 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:25 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:25 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:307f8152a55ef1e9eeb1acbbee7bc81232615329eaeb00d8dd93b46be297f34c`  
		Last Modified: Fri, 08 May 2026 18:24:07 GMT  
		Size: 49.3 MB (49302320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066b5036abddef18ea16cf7d398691ec77b7d6fe0418ccabe5372f7a00c08bd6`  
		Last Modified: Tue, 12 May 2026 21:46:45 GMT  
		Size: 55.2 MB (55198694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97df66a0490e776297a0c8cdf5329b38a507d7c3d14e2b7e77c924e8489c5360`  
		Last Modified: Tue, 12 May 2026 21:46:46 GMT  
		Size: 85.6 MB (85570954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240c90b53ec2efa96cb648918f9b4f68c964372adfa6b355b0f1153ccacdeb2e`  
		Last Modified: Tue, 12 May 2026 21:46:42 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:3341cae0cd678ff55bd7490de120527d7a09d07b3e5faf8b7bd6f714ff4fbe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7606032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17aafb482caf24a283b3b7923050d8b4525e4a0036a03cb5428a762d543a82bc`

```dockerfile
```

-	Layers:
	-	`sha256:e57ab3bd48ae11a9ffa5f1f3006f8024ed375bd1db43f9e1a8535f31e3dbcb16`  
		Last Modified: Tue, 12 May 2026 21:46:43 GMT  
		Size: 7.6 MB (7591708 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0c3213b229538fc0b0227ff93c1dc398e4cafcd94d5d2a4f1e4dccad465145eb`  
		Last Modified: Tue, 12 May 2026 21:46:42 GMT  
		Size: 14.3 KB (14324 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f2d6c4b3d5d5ee1b77aedc6cacee4ef98369efa87108cd4342824110b1937a21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.3 MB (189326700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db52aee449aff288852833b93d97706898cc41d6466f1211b9c0263984936a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:45:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:45:56 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:45:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:45:56 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:45:56 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:46:13 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:46:14 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:46:14 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b5d74b688654dda99557234223479d1600781c2797759908abb12a2e782ab1ad`  
		Last Modified: Fri, 08 May 2026 18:26:51 GMT  
		Size: 49.7 MB (49669445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e7613ccf9ecb0c52f60814e3d5dfe72f7f5990f515671f315be3180d037b78c`  
		Last Modified: Tue, 12 May 2026 21:46:35 GMT  
		Size: 54.3 MB (54272958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f864622bf3705bf73be7c0d001fde560052fe4ed0dd600ca1775f1e6c8f0d8a`  
		Last Modified: Tue, 12 May 2026 21:46:36 GMT  
		Size: 85.4 MB (85383649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1fb7e2a549a3ef6be54b4e5329b79991cb6f88edc130e89185b14907c80467`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:e274944fac37eb54324261d23bd3302c923584d4ceca85648af0606b2cc7c38b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7613879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b379f653314cd1e894ef0d952bf7b39ed2a128d989d1856107aeb5655446ccb`

```dockerfile
```

-	Layers:
	-	`sha256:b73cf3fccc791b7f7c091dfa8c95049aa39e4cb656775f32070cac9f126dbca1`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 7.6 MB (7599438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e00b7de7387f8eac6d9aefa8c0340cdc08c79cd65b2a96559eb0973a5e2f11`  
		Last Modified: Tue, 12 May 2026 21:46:31 GMT  
		Size: 14.4 KB (14441 bytes)  
		MIME: application/vnd.in-toto+json

### `clojure:temurin-8-tools-deps-trixie` - linux; ppc64le

```console
$ docker pull clojure@sha256:027d717594e470717fc7449632b7499498852698ec70b2f8d1b7f71931c775e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 MB (196779330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91eb38a6b80d83fa9ee99e4e23ed4a0acd2279e05b80d87f95a707f63883670e`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 12 May 2026 21:49:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 12 May 2026 21:49:10 GMT
COPY /opt/java/openjdk /opt/java/openjdk # buildkit
# Tue, 12 May 2026 21:49:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2026 21:49:10 GMT
ENV CLOJURE_VERSION=1.12.4.1618
# Tue, 12 May 2026 21:49:11 GMT
WORKDIR /tmp
# Tue, 12 May 2026 21:54:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap && rm -rf /var/lib/apt/lists/* && curl -fsSLO https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "8a49ab11a639ce1d49e5459a7bfa8fcc74684ad3bc9acd181e3adc7a662918cf *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl # buildkit
# Tue, 12 May 2026 21:54:46 GMT
COPY rlwrap.retry /usr/local/bin/rlwrap # buildkit
# Tue, 12 May 2026 21:54:46 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:95ea8643a6311b39c5ca6b858ab22e7e7fb5819831b6070e3d6390a0ebf1be97`  
		Last Modified: Fri, 08 May 2026 19:46:54 GMT  
		Size: 53.1 MB (53123165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6108e5c2a2245ec0c51d22b23687faec2598356811a7675057929aac5f8deda`  
		Last Modified: Tue, 12 May 2026 21:50:14 GMT  
		Size: 52.7 MB (52669152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798c5d59fd7a62c2128257f8308aa0a9b3a391b47efb8743a888e358124cbf24`  
		Last Modified: Tue, 12 May 2026 21:55:36 GMT  
		Size: 91.0 MB (90986364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5411a399ceeaad9b2efaef8de3efb3c8e58af8d1997dd9ebcae0d0c6170a589c`  
		Last Modified: Tue, 12 May 2026 21:55:34 GMT  
		Size: 617.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `clojure:temurin-8-tools-deps-trixie` - unknown; unknown

```console
$ docker pull clojure@sha256:a98fc0d2ae20e6642666ec06291a7326e9e88186128cdfebbba3c8233e8ffa18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7611096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc3d66fa6cfac27258b2556ad061fe175affd1ce39d482b8a6e7f20c9d13cf2`

```dockerfile
```

-	Layers:
	-	`sha256:f3274843f0fc7c43d66d6811aea298404bcfa1d340dae00e09b0fff955362f7a`  
		Last Modified: Tue, 12 May 2026 21:55:35 GMT  
		Size: 7.6 MB (7596724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a16492f2707799caf97e810fd886c1398b84b53ec873329cbfc7641c53b0ce0`  
		Last Modified: Tue, 12 May 2026 21:55:34 GMT  
		Size: 14.4 KB (14372 bytes)  
		MIME: application/vnd.in-toto+json
