## `aerospike:ee-5.7.0.7`

```console
$ docker pull aerospike@sha256:30ff0d6f7c623812e104ed9a1afd95d9867b21bf2fc89a8642fbf798019bae42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `aerospike:ee-5.7.0.7` - linux; amd64

```console
$ docker pull aerospike@sha256:5b9e21b5eaa328b2671968fd261fa7280fa445c1a4dbb8b9ca16e0f4bce5b6bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83516717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ff1f422dfefc6a58fb43ca3fa8959c429a54cd66448caf5fd5166fc4b68875`
-	Entrypoint: `["\/usr\/bin\/dumb-init","--","\/entrypoint.sh"]`
-	Default Command: `["asd"]`

```dockerfile
# Tue, 12 Oct 2021 01:21:05 GMT
ADD file:910392427fdf089bc26b64d6dc450ff3d020c7c1a474d85b2f9298134d0007bd in / 
# Tue, 12 Oct 2021 01:21:05 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 02:07:29 GMT
ENV AEROSPIKE_VERSION=5.7.0.7
# Tue, 12 Oct 2021 02:07:29 GMT
ENV AEROSPIKE_SHA256=c0b51e4389b7809bf059015164e1f2ae26dae9205b53ad5dca121a071980ba8e
# Tue, 12 Oct 2021 02:07:49 GMT
RUN apt-get update -y   && apt-get install -y iproute2 procps dumb-init wget python python3 python3-distutils lua5.2 gettext-base libldap-dev libcurl4-openssl-dev   && wget "https://www.aerospike.com/enterprise/download/server/${AEROSPIKE_VERSION}/artifact/debian10" -O aerospike-server.tgz   && echo "$AEROSPIKE_SHA256 *aerospike-server.tgz" | sha256sum -c -   && mkdir aerospike   && tar xzf aerospike-server.tgz --strip-components=1 -C aerospike   && dpkg -i aerospike/aerospike-server-*.deb   && dpkg -i aerospike/aerospike-tools-*.deb   && mkdir -p /var/log/aerospike/   && mkdir -p /var/run/aerospike/   && rm -rf aerospike-server.tgz aerospike /var/lib/apt/lists/*   && rm -rf /opt/aerospike/lib/java   && dpkg -r wget ca-certificates openssl xz-utils  && dpkg --purge wget ca-certificates openssl xz-utils  && apt-get purge -y   && apt autoremove -y   && find /usr/bin/ -lname '/opt/aerospike/bin/*' -delete   && find /opt/aerospike/bin/ -user aerospike -group aerospike -exec chown root:root {} +   && mv /opt/aerospike/bin/* /usr/bin/   && rm -rf /opt/aerospike/bin
# Tue, 12 Oct 2021 02:07:50 GMT
COPY file:7d75174e09b209cf7f56b715636c2b8e08dd083d548e8cdc8517cabd512600b5 in /etc/aerospike/aerospike.template.conf 
# Tue, 12 Oct 2021 02:07:50 GMT
COPY file:31b6a51a1d9d91f22433472f07f6ddfe3cea3bb07f460dd69c4187bc7fd20fdf in /entrypoint.sh 
# Tue, 12 Oct 2021 02:07:50 GMT
EXPOSE 3000 3001 3002
# Tue, 12 Oct 2021 02:07:51 GMT
ENTRYPOINT ["/usr/bin/dumb-init" "--" "/entrypoint.sh"]
# Tue, 12 Oct 2021 02:07:51 GMT
CMD ["asd"]
```

-	Layers:
	-	`sha256:b380bbd43752f83945df8b5d1074fef8dd044820e7d3aef33b655a2483e030c7`  
		Last Modified: Tue, 12 Oct 2021 01:26:51 GMT  
		Size: 27.1 MB (27139510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8c8779ae173ba24709980e3bdf39508b2d17af26098189f35779248371ccc1`  
		Last Modified: Tue, 12 Oct 2021 02:08:35 GMT  
		Size: 56.4 MB (56375126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b203a8f1d71482eb1dc85b1473fba3f2660edb8871756576c20d1c47ea85b6f9`  
		Last Modified: Tue, 12 Oct 2021 02:08:26 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55e4617fc883c16e069d05f82c7fe94ea0caa651467fdec9fbee422a00bc66`  
		Last Modified: Tue, 12 Oct 2021 02:08:26 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
