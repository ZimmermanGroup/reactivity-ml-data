# reactivity-ml-data
datasets to accompany the paper "What does the machine learn? Knowledge representations of chemical reactivity"

Each row of each dataset corresponds to a chemical reaction.

Meaning of each column of the feature vector (hierarchical notation):

Overall feature vector (all columns for one row of dataset, size=195) ::= ["heat of reaction"][add_moves (type=drive_coord_pooled)][break_moves (type=drive_coord_pooled)]

drive_coord_pooled (size=97) ::= [max_pool_vals (type=drive_coord)][min_pool_vals (type=drive_coord)][mean_pool_vals (type=drive_coord)]

drive_coord (size=32) ::= [atom_one (type=atom)][atom_two (type=atom)]

atom (size=16) ::= [nbo_features (type=nbo)][graph_features (type=graph)]

nbo (size=2) ::= ["partial charge"]["partial_hybridization"]

graph (size=14) ::= [self (type=basic_info)][neighbor_one (type=basic_info)]["bond_order_one"][neighbor_two (type=basic_info)]["bond_order_two"][neighbor_three (type=basic_info)]["bond_order_three"][neighbor_four (type=basic_info)]["bond_order_four"]

basic_info (size=2) ::= ["atomic number"]["coordination number"]
