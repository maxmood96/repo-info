## `aerospike:ee-6.0.0.4`

```console
$ docker pull aerospike@sha256:dcb3a3bed769b7c9729512f15bb456eb69260c5f15efd51d01c9c1e41cbe2fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-6.0.0.4` - linux; amd64

```console
$ docker pull aerospike@sha256:785345a0e233fa3bdec0a787ba7f2eb76745622567a1d73d6416624d66aaad9e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104255740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30363909d4f33c18236739a392c774e7a4781563e9e227ac39bb69efb1e348e3`
-	Entrypoint: `["\/usr\/bin\/as-tini-static","-r","SIGUSR1","-t","SIGTERM","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 23 Aug 2022 00:21:10 GMT
ADD file:baca493d7744d12304f6d9c7b6ec0800453a0ba02cbf4005ec35c7b921adf0c4 in / 
# Tue, 23 Aug 2022 00:21:10 GMT
CMD ["bash"]
# Tue, 23 Aug 2022 00:44:08 GMT
ENV AEROSPIKE_VERSION=6.0.0.4
# Tue, 23 Aug 2022 00:44:08 GMT
ENV AEROSPIKE_SHA256=2e7db8e35aa8d9214ab59ead9b8455a824c236d57a44aa00f25de1012ed2d6d9
# Tue, 23 Aug 2022 00:44:08 GMT
ENV AS_TINI_SHA256=d1f6826dd70cdd88dde3d5a20d8ed248883a3bc2caba3071c8a3a9b0e0de5940
# Tue, 23 Aug 2022 00:44:31 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget https://github.com/aerospike/tini/releases/download/1.0.1/as-tini-static -O /usr/bin/as-tini-static   && echo "$AS_TINI_SHA256 /usr/bin/as-tini-static" | sha256sum -c -   && chmod +x /usr/bin/as-tini-static   && wget "https://download.aerospike.com/artifacts/aerospike-server-enterprise/${AEROSPIKE_VERSION}/aerospike-server-enterprise-${AEROSPIKE_VERSION}-debian10.tgz" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && if [ -d '/opt/aerospike/bin/asadm' ];   then   mv /opt/aerospike/bin/asadm /usr/lib/;   ln -s /usr/lib/asadm/asadm /usr/bin/asadm;   fi   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 23 Aug 2022 00:44:31 GMT
COPY file:f56e2e33c0b4bb66affff75053eaed44661e723b8b33d3ef3c10e305b506c350 in /etc/aerospike/aerospike.template.conf 
# Tue, 23 Aug 2022 00:44:32 GMT
COPY file:697e2123680798e87da7a3f98d1d70e76ffec66f0e1aafa90ff25047a11cca52 in /entrypoint.sh 
# Tue, 23 Aug 2022 00:44:32 GMT
EXPOSE 3000 3001 3002
# Tue, 23 Aug 2022 00:44:32 GMT
ENTRYPOINT ["/usr/bin/as-tini-static" "-r" "SIGUSR1" "-t" "SIGTERM" "--" "/entrypoint.sh"]
# Tue, 23 Aug 2022 00:44:32 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:2238450926aa858e592e60bb5d68dd26eeab8a984eee45505ca89d2022e3b450`  
		Last Modified: Tue, 23 Aug 2022 00:25:43 GMT  
		Size: 27.1 MB (27138330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86f717a696c279610c79446e55f77aa2b547d8f9d6d45a98c19923aa3936181`  
		Last Modified: Tue, 23 Aug 2022 00:45:23 GMT  
		Size: 77.1 MB (77115529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55930335680eccb1a6d086cfdbe7d70b64990f55b743f9e78c4fc07aa1679ee3`  
		Last Modified: Tue, 23 Aug 2022 00:45:11 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a963d16299f59e05e544314a755bf992efb3467d84ebe07f90b89d7aac119651`  
		Last Modified: Tue, 23 Aug 2022 00:45:11 GMT  
		Size: 839.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
