## `maven:3-sapmachine-22`

```console
$ docker pull maven@sha256:3c2ba6868e3c89fedacb54083151061c8adfceff250478628cc09281b9a78fde
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-sapmachine-22` - linux; amd64

```console
$ docker pull maven@sha256:13f8679533ff56edfaaafdfb4c0c8185b3fac741bf0d4625523e3f1c3276b522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276390306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21e3713614f652e6b44818ce3e3b60218dd21cb84ff7c81ff76ad2ead8b2f234`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835f8f35c95610ca5687d9be749f7b06ba9d6bfd97fd5f43b56be3df494c0022`  
		Last Modified: Tue, 25 Jun 2024 22:57:48 GMT  
		Size: 213.8 MB (213790435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d8d805a5c0fc83e27b2318c498860d607e64417eab02a987e8383f4022cb45`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 23.7 MB (23731863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b94d27e9beb10a529296b625e766e7c882908a473f00796a730ab52bf566f5d`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 9.2 MB (9161816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e28f0460d5058845c41e208242469469472afe034608e90f2a270056bae97f8`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f29c2678c409e5ded6891e8ba5a0cb47210f259674a7953c4a0af418f551974b`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:bc449b52be5068a0539c354bd565c2bf08b48d38297d0e151ee96c4ebc1f67b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4064582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c6e478123c5689f3b6f669fae8da354c6ccd6101dc9118d82efe5804f9f78f5`

```dockerfile
```

-	Layers:
	-	`sha256:21f568ef61967232224322347bd358ab293e54e0e59dc75f77842d61ea09997f`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 4.0 MB (4048113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaafca870a5103ad9bd622d232e50d25ec7cbbe8a666d22afc5800dc376eb667`  
		Last Modified: Tue, 02 Jul 2024 09:09:31 GMT  
		Size: 16.5 KB (16469 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3a212093df08e16e1745090040a6834383c5c5eac9b4e3bf5cf188ed02a395ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **273.6 MB (273606392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d335bff4aca0d5bfad1294403813e97b8e66e08d018217ab60e085dfe6513fba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8be052ef5d257bce29bcdac702f21606f8f820cb3a9f5c2aaec6f245d396016`  
		Last Modified: Tue, 25 Jun 2024 23:50:20 GMT  
		Size: 211.8 MB (211781332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24a1eae3ccb1048925d0122de09aa5b2035d93abdfd0b60e7e8cf19e9fcde4f`  
		Last Modified: Wed, 03 Jul 2024 10:44:21 GMT  
		Size: 23.8 MB (23819197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b70e8be03b5bea5714413056f32e71f52dec0ac78f0333bc33658294e5b064`  
		Last Modified: Wed, 03 Jul 2024 10:44:21 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c2da38671d35fff4293b0cf5ad129ef9a077e19b763cda0d3d67cd4570ab02`  
		Last Modified: Wed, 03 Jul 2024 10:44:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc340fe11c3138e769ffe2302b6890f3ddb92c00d6caff255d5e6fe16166a650`  
		Last Modified: Wed, 03 Jul 2024 10:44:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:b7eb6eca401981a3672716deb568799aecd0d215edb4fbf30a26d3ec1ba02a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4071201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3637fde809f12c807a22b492d64d8cf3bdf47bc84d0f70bc73de7b51c198ac37`

```dockerfile
```

-	Layers:
	-	`sha256:8d4232db9beef706d3d8def627d8337a5f8cf21a11b2629604e164e532c8a80d`  
		Last Modified: Wed, 03 Jul 2024 10:44:21 GMT  
		Size: 4.1 MB (4054007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ca63d3b2cc0f0047020929a625f12f8dc2ab0803b7f9a62c2fd779eccf90b27`  
		Last Modified: Wed, 03 Jul 2024 10:44:20 GMT  
		Size: 17.2 KB (17194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-sapmachine-22` - linux; ppc64le

```console
$ docker pull maven@sha256:333717e066421964ed51cc91deb8209d0bfba8c40ce7430f9d409ff9d1b18154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286524625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:802ba3ad3cd4f680d5849542902b03f2b74321d5caae8494196a2afa0458b9ac`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 May 2024 10:06:58 GMT
ARG RELEASE
# Mon, 13 May 2024 10:06:58 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 May 2024 10:06:58 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 13 May 2024 10:06:58 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Mon, 13 May 2024 10:06:58 GMT
CMD ["/bin/bash"]
# Mon, 13 May 2024 10:06:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 13 May 2024 10:06:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Mon, 13 May 2024 10:06:58 GMT
CMD ["jshell"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccc34635659453a00507f117554b35de0cc6055a7e9f1d9d5e220ab8d70f5ca`  
		Last Modified: Wed, 26 Jun 2024 00:06:30 GMT  
		Size: 215.0 MB (214996096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005e301411736b41b91244a5c793f89fb38d21138580f554bc0df8d9fed9c9b7`  
		Last Modified: Thu, 27 Jun 2024 19:13:43 GMT  
		Size: 27.9 MB (27859673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0ec3270d5dc4b2e1269d57243e059f2f12b82a894a8610f2bec852bf494d28`  
		Last Modified: Thu, 27 Jun 2024 19:13:43 GMT  
		Size: 9.2 MB (9161782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe9107454f39bc6b66a51bd23bd9e1ca77af904614e5d27ff5c891ff0f5fa5e4`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 857.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc95700e72527ac65427b86e8f3f8c7359104ba83083f8657920f6142d42df6b`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-sapmachine-22` - unknown; unknown

```console
$ docker pull maven@sha256:c22fcb8907b48776648d487f420406d00d0351e6b31b41629cb02a064634a361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.1 MB (4068872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2663eedb15688796c633e73522012471f7b2487815a6db5aa5ed18ee9c46035e`

```dockerfile
```

-	Layers:
	-	`sha256:0455b0caebb15a9e638ff43b657085228718f0e3cb5d43a0103b1febf172c44b`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 4.1 MB (4052323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2be37166a14da692eb9e48073e39fc44d935572d3b0ee35de81f8f7fcde1d0eb`  
		Last Modified: Thu, 27 Jun 2024 19:13:42 GMT  
		Size: 16.5 KB (16549 bytes)  
		MIME: application/vnd.in-toto+json
