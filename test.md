graph TD
    %% Acteurs Externes
    C((Client))
    
    %% Acteurs Internes
    AV[Agent Vendeur]
    SF[Service Financier]
    SEC[Secrétariat/Hotline]

    %% Flux Phase 1 & 2
    C -- 1. Critères / Modifs --> AV
    AV -- 2. Propositions / Devis --> C
    
    %% Flux Phase 3 & 4
    C -- 3. Accord & Infos Perso --> AV
    
    %% Flux Phase 5
    C -- 4. Paiement --> SF
    SF -- 5. Facture / Reçu --> C
    
    %% Flux Phase 6
    SF -. 6. Confirmation Solde .-> AV
    AV -- 7. Pack Voyage (Billets/Bons) --> C
    
    %% Flux Phase 7
    C -- 8. Appel Assistance --> SEC
