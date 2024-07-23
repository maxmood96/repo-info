## `openjdk:24-ea-7-jdk`

```console
$ docker pull openjdk@sha256:31dabaeba1cb7026ee74bb21b8f34390a664bc863c0d65a671e5ec4c59d799ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-ea-7-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:2dcd2a56db5990767ebad7d0e3cd6174b43421a0725efc9383969a1a3d3b37d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.4 MB (298390686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b836db5a9448e2d444fffcb439c0a7ec33747634cf4b5b62fdb87ba12fda67a9`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 08 Jul 2024 23:20:26 GMT
ADD file:61bb1ff5b435c8d45a692de54806f1a1d44cbd176c28877e360a68f4d0e7de6f in / 
# Mon, 08 Jul 2024 23:20:26 GMT
CMD ["/bin/bash"]
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Sat, 20 Jul 2024 00:52:05 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 20 Jul 2024 00:52:05 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jul 2024 00:52:05 GMT
ENV JAVA_VERSION=24-ea+7
# Sat, 20 Jul 2024 00:52:05 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-x64_bin.tar.gz'; 			downloadSha256='d175c4cfc7ab8306b42cf88fe0e60b2b827a2106c026ae6d2a3f2e51bbcb60d0'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_linux-aarch64_bin.tar.gz'; 			downloadSha256='5df46f7b64a38a7a34e1b283f6c37b57f8238567b81c3db0f127f348f4842977'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Sat, 20 Jul 2024 00:52:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d9a40b27c30f626a234b4038d1370cabaed0e37737d0a56e3ea84710f110f14c`  
		Last Modified: Mon, 08 Jul 2024 23:21:45 GMT  
		Size: 49.0 MB (48993736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2920cc2c11af612b622d60cb0efe552bd6ba226ef084ef8060c17399289d7444`  
		Last Modified: Mon, 22 Jul 2024 21:00:06 GMT  
		Size: 37.9 MB (37871931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec9a29a9c955047ef4c9646b22e92de51ea17b8c54d6d2c853b342491db359dc`  
		Last Modified: Mon, 22 Jul 2024 21:00:09 GMT  
		Size: 211.5 MB (211525019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-7-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:04c7ca6f50bf7cfc4278ebd857b96731549f864ad4e8003c3f6a265125d3cdde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3377698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f68a61438acc4f9ab6efec86712d89c3422594234885843e06609a1757a067eb`

```dockerfile
```

-	Layers:
	-	`sha256:a8bf82b5e8d260d4ca1fc7a06ba5233d304aacf6b96e1af06abfff352a08010c`  
		Last Modified: Mon, 22 Jul 2024 21:00:06 GMT  
		Size: 3.4 MB (3358195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fa193321b0932b134f82eaae2d765278bd321d09b0fd232ad9247878a998df8`  
		Last Modified: Mon, 22 Jul 2024 21:00:05 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-7-jdk` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:871cd303c209d07e6f8197839f19e4edbad83fa79b88e5e5f51304edc12613bc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346993191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73310b0659fcfeb11c9af25284339d5f0c9adfcd38cbc857ded98dadbc51167b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 22 Jul 2024 22:08:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 22:10:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 22:10:23 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 22 Jul 2024 22:10:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 22:10:30 GMT
ENV JAVA_VERSION=24-ea+7
# Mon, 22 Jul 2024 22:10:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_windows-x64_bin.zip
# Mon, 22 Jul 2024 22:10:32 GMT
ENV JAVA_SHA256=e6ea3b3cd29d732dbe15fd95b7719200d69fff9e9f42a09fc5dc4fc3bd5fea12
# Mon, 22 Jul 2024 22:11:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 22:11:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff11603de76dd8a343f7d2e9772bc77dece0072d9569cbcd95e485e71178689`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259175014e57ba688d182f51a0e9721d75e0b0febb6b753c3e66d67ef4aa921b`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 372.3 KB (372258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c77dc12a95152c648cfd642d625ac9bd276e1d44bd01c10e520dc4485e1d544`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76b5fd23a055c817570d4c15651dd37b694728d5c77df94ed4ab552a98d74c7`  
		Last Modified: Mon, 22 Jul 2024 22:11:07 GMT  
		Size: 322.9 KB (322875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b816afafd58f833f8ba442090de2ac9b5e07bec5a9eecc2c5856742d150a2`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58beef9dda82dcc7ecb42a0c468e2f46dd7eb38c59c17840d9647b7394831a33`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e697456abe140aaa590dbf208b27bc313a621442cc94a28c5acad14ff46803c2`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45091fc70e1a8cac8d32f29bd7df18318653d3437f288f0834d29f8fb4be1ff2`  
		Last Modified: Mon, 22 Jul 2024 22:11:17 GMT  
		Size: 206.7 MB (206689975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84aaa5254d1d5e440c194c36245ab44b4757b530aeaabc0034a4c3d7d0d1afe7`  
		Last Modified: Mon, 22 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-7-jdk` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:63055ae54bd73592c96e8d351dd15c94adc971ecd979a9a4d39e80829c4d7c79
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2446019041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:526ad0aa9e2dd4d541f6022dae9906396d45ebde11a2000d7e4ee961336fe454`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 22 Jul 2024 20:59:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jul 2024 21:01:40 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:01:40 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 22 Jul 2024 21:02:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:02:12 GMT
ENV JAVA_VERSION=24-ea+7
# Mon, 22 Jul 2024 21:02:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/7/GPL/openjdk-24-ea+7_windows-x64_bin.zip
# Mon, 22 Jul 2024 21:02:13 GMT
ENV JAVA_SHA256=e6ea3b3cd29d732dbe15fd95b7719200d69fff9e9f42a09fc5dc4fc3bd5fea12
# Mon, 22 Jul 2024 21:03:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jul 2024 21:03:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a324fbdfaaec19a11b8db2f41af298db0f43eca4654bbbf10e4b7b37071336ee`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9287ce7bf1b39b687283e9bfd0266eceb4e07631d1371ae71e45241047f5e8`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 506.9 KB (506930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a6d24720e8fa902eea7434f0372d1aebaff0ec5f6961f9f468445fac6ae8b4`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1596e210d84e1a6d680409424af13fa06f77777ffc1824371da481e1c0380319`  
		Last Modified: Mon, 22 Jul 2024 21:03:21 GMT  
		Size: 350.5 KB (350468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72a0c2b5a97c9ecc1a29bc28f4fd1fa3da64748149bf5209bf99da390c52191`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466eca85bfc0d7c04f6b609fc0902cb12801cf02d31d01339361121ace9bc89f`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7d1eab0223919a362c0382273e07c5fd67f80d39fc85cd9fd508f3c74d718c4`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243afa0977d08622fa7e1849a775112589966699e81eecc2ce31dca631729608`  
		Last Modified: Mon, 22 Jul 2024 21:03:30 GMT  
		Size: 206.7 MB (206724441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b889e74c1f5b2e925eb670de44dafc9229d8d964e249f62e5af405c469a3f47`  
		Last Modified: Mon, 22 Jul 2024 21:03:19 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
