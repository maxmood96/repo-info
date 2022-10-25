## `maven:sapmachine`

```console
$ docker pull maven@sha256:58dd425465a80f566184b168092287b8004b1e204b0e679c2daf804a66cefb1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:sapmachine` - linux; amd64

```console
$ docker pull maven@sha256:4c688225c3252099ab66fb5f9ec8a2fcfc22f35ffcf8364ed96f162e117a8bc7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.3 MB (275335005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd00610603cc659a2d5eb6da04720a318bd5c6b969e49a158fec73eb2433ace`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 25 Oct 2022 01:53:34 GMT
ADD file:7633003155a1059419aa1a6756fafb6e4f419d65bff7feb7c945de1e29dccb1e in / 
# Tue, 25 Oct 2022 01:53:35 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 18:28:52 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:29:55 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.5     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 18:29:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Tue, 25 Oct 2022 18:29:56 GMT
CMD ["jshell"]
# Tue, 25 Oct 2022 19:57:36 GMT
RUN apt-get update     && apt-get install -y curl git     && rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 19:57:36 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 25 Oct 2022 19:57:36 GMT
ARG USER_HOME_DIR=/root
# Tue, 25 Oct 2022 19:57:37 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 25 Oct 2022 19:57:37 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 25 Oct 2022 19:57:43 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 25 Oct 2022 19:57:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 25 Oct 2022 19:57:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 25 Oct 2022 19:57:43 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 25 Oct 2022 19:57:43 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 25 Oct 2022 19:57:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 25 Oct 2022 19:57:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eaead16dc43bb8811d4ff450935d607f9ba4baffda4fc110cc402fa43f601d83`  
		Last Modified: Fri, 21 Oct 2022 03:03:39 GMT  
		Size: 28.6 MB (28577834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce68e21cf06ac72066ade930bdfb3d7e3b9da0cc4d6d121a841d01b83627b971`  
		Last Modified: Tue, 25 Oct 2022 18:30:47 GMT  
		Size: 7.9 MB (7923897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf96790da5de2aa26ca5ce95a3d24a9954d70bf5b1a588e481725a84cfda001`  
		Last Modified: Tue, 25 Oct 2022 18:31:25 GMT  
		Size: 198.0 MB (198038200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960f237e2c66d6afa76e5c985a2faede2268b714654f27ef6da607f9105a11a2`  
		Last Modified: Tue, 25 Oct 2022 20:00:10 GMT  
		Size: 32.1 MB (32054360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfeea0f7ad858a8de616891c4ffcefd185698fcceb15c66fcb033e97e04df8e`  
		Last Modified: Tue, 25 Oct 2022 20:00:06 GMT  
		Size: 8.7 MB (8739503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8457258f59ca4f95269ae234edb51b6357d9fbb124a8b5e755a05eda2c7eaf`  
		Last Modified: Tue, 25 Oct 2022 20:00:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a87da97d5d2e8327fbfe3d09330a7336f8c452b80991656fecbe49a4de2a599a`  
		Last Modified: Tue, 25 Oct 2022 20:00:07 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
